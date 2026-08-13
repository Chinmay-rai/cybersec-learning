# Day 69 – Wazuh SOC Lab Architecture and First Detection

## What I Did

* Completed the core endpoint integration of my Wazuh SOC lab
* Connected a Windows 11 VM to the Wazuh Manager
* Built a resource-efficient operating workflow for the Wazuh stack
* Created **Low-RAM** and **Full Investigation** modes for the lab
* Troubleshot Windows Agent connectivity and registration
* Increased Linux swap space to provide additional memory headroom
* Generated my first controlled Windows security event and successfully detected it in Wazuh

---

## Lab Architecture

The lab consists of a **Kubuntu host** running the Wazuh server stack and a **Windows 11 virtual machine** acting as the monitored endpoint.

```text
                         SOC LAB
                            │
             ┌──────────────┴──────────────┐
             │                             │
       Kubuntu Host                  Windows 11 VM
       192.168.1.51                  SOC-WIN01
             │                         Agent 006
             │                             │
             │                         Wazuh Agent
             │                             │
             └──────────────┬──────────────┘
                            │
                     TCP 1514 / Secure
                            │
                            ▼
                    ┌─────────────────┐
                    │  Wazuh Manager  │
                    │    Detection    │
                    │     Engine      │
                    └────────┬────────┘
                             │
                    Alert / Event Data
                             │
                             ▼
                    ┌─────────────────┐
                    │  Wazuh Indexer  │
                    │  Data Storage   │
                    └────────┬────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │ Wazuh Dashboard │
                    │ Visualization & │
                    │ Investigation   │
                    └─────────────────┘
```

### Component Roles

| Component           | Role                                                                |
| ------------------- | ------------------------------------------------------------------- |
| **Wazuh Agent**     | Collects security telemetry from the Windows endpoint               |
| **Wazuh Manager**   | Receives, decodes, analyzes events and applies detection rules      |
| **Wazuh Indexer**   | Stores alert and event data for searching and visualization         |
| **Filebeat**        | Ships Wazuh alert data to the Indexer                               |
| **Wazuh Dashboard** | Provides visualization, searching, threat hunting and investigation |
| **Windows 11 VM**   | Simulated SOC endpoint being monitored                              |
| **Kubuntu Host**    | Runs the Wazuh infrastructure                                       |

---

## Low-RAM Operating Mode

Because the lab is running on a system with **8 GB of physical RAM**, running the complete Wazuh stack together with a Windows VM can create significant memory pressure.

I therefore implemented a **Low-RAM Mode**.

```text
Windows VM
    │
    ▼
Wazuh Agent 🟢
    │
    ▼
Wazuh Manager 🟢
    │
    └── Detection / Alert Generation


Wazuh Indexer  🔴
Filebeat       🔴
Dashboard      🔴
```

In this mode:

* The Windows Agent remains active
* The Wazuh Manager remains active
* The Manager continues receiving and analyzing endpoint events
* The Indexer, Filebeat and Dashboard are stopped
* Memory usage is significantly reduced
* Alerts can still be generated and inspected from the Manager's local alert logs

This mode is primarily used for:

> **Generating activity → Collecting telemetry → Detecting events**

---

## Full Investigation Mode

When graphical investigation is required, the remaining components are started.

```text
Windows VM
    │
    ▼
Wazuh Agent 🟢
    │
    ▼
Wazuh Manager 🟢
    │
    ▼
Filebeat 🟢
    │
    ▼
Wazuh Indexer 🟢
    │
    ▼
Wazuh Dashboard 🟢
```

This mode is used for:

> **Searching → Visualizing → Investigating → Analyzing alerts**

---

## Lab Scripts

To avoid manually starting and stopping individual services, I created two scripts.

### `wazuh-memory-save`

Switches the system to **Low-RAM Mode** by stopping:

* Wazuh Dashboard
* Filebeat
* Wazuh Indexer

while keeping the Manager running.

### `wazuh-full-start`

Starts:

* Wazuh Manager
* Wazuh Indexer
* Filebeat
* Wazuh Dashboard

---

## Windows Endpoint Integration

Configured a Windows 11 VM as the monitored endpoint:

```text
Agent Name: SOC-WIN01
Agent ID:   006
OS:         Windows 11 Pro
Wazuh:      4.14.7
```

### Connectivity Troubleshooting

Initially, the Windows Agent repeatedly attempted to connect but was never registered as active.

Troubleshooting included:

* Verifying the Wazuh Agent service
* Verifying the Manager address
* Testing ICMP connectivity
* Testing TCP connectivity to port `1514`
* Verifying `wazuh-remoted` was running
* Verifying port `1514` was listening
* Checking the Windows Agent logs
* Checking the Wazuh Manager logs
* Verifying the authentication key

The key discovery was:

```text
Message from '192.168.1.51' not allowed.
Cannot find the ID of the agent.
Source agent ID is unknown.
```

The Windows VM was using **VirtualBox NAT**, causing the Manager to see the connection from a different source address.

The endpoint was therefore registered using:

```text
IP: any
```

After generating a new authentication key and configuring it on Windows, the agent successfully connected.

### Final Status

```text
Agent 006
SOC-WIN01
Status: Active
```

---

## Memory Management

During testing, the host experienced severe memory pressure while running the Windows VM, Wazuh and other applications.

Linux generated an OOM event and terminated Chrome:

```text
Out of memory: Killed process ... (chrome)
```

Wazuh detected this as a **Level 12 alert**.

To provide additional memory headroom, the Linux swapfile was increased from:

```text
512 MB → 10 GB
```

The swapfile is configured to automatically activate at boot through `/etc/fstab`.

> **Swap is being treated as a safety buffer rather than a replacement for physical RAM.**

---

## First Controlled Security Detection

After successfully connecting the Windows endpoint, I generated a controlled authentication failure.

Windows auditing was verified with:

```powershell
auditpol /get /subcategory:"Logon"
```

which showed:

```text
Logon    Success and Failure
```

I then intentionally entered an incorrect password once on the Windows login screen.

This generated a Windows failed authentication event.

### Wazuh Detection

The event appeared in the Wazuh Threat Hunting interface after filtering for:

```text
agent.id: 006
```

The resulting alert was:

```text
Agent:       SOC-WIN01
Event:       Logon Failure - Unknown user or bad password
Rule ID:     60122
Level:       5
```

The dashboard confirmed:

```text
Total alerts:           1
Authentication failure: 1
Level 12+ alerts:       0
```

This demonstrated the complete detection pipeline:

```text
Incorrect Password
       ↓
Windows Security Event
       ↓
Wazuh Agent
       ↓
Wazuh Manager
       ↓
Detection Rule 60122
       ↓
Authentication Failure Alert
       ↓
Wazuh Indexer
       ↓
Wazuh Dashboard
       ↓
SOC Analyst Investigation
```

---

## Key Learning

This exercise demonstrated that **Wazuh does not require the Dashboard to perform detection**.

The **Wazuh Manager** is responsible for analyzing incoming telemetry and applying detection rules, while the Indexer and Dashboard provide the storage, search and investigation layer.

This allowed the lab to operate in **Low-RAM Mode** while still collecting and detecting security events.

It also demonstrated an important SOC principle:

> **A security alert is not automatically an attack.**

The analyst must investigate the context of the alert, determine whether the activity is expected or suspicious, and correlate it with other evidence.

---

## Current Lab State

```text
Windows VM / SOC-WIN01
        │
        │ Wazuh Agent
        ▼
Wazuh Manager
        │
        ├── Low-RAM Mode → Detection / Collection
        │
        └── Full Mode → Investigation / Dashboard
```

The core Wazuh SOC pipeline is now operational, and the first controlled Windows security event has been successfully detected and investigated.

---

## Next Step

* [ ] Generate additional Windows security activity
* [ ] Investigate Wazuh alerts from the Windows endpoint
* [ ] Explore Wazuh rules and detection logic
* [ ] Begin investigating authentication and endpoint activity through the Wazuh Dashboard

---

**Day 69 Status:** 🟢 **Core Wazuh SOC Pipeline Operational**
