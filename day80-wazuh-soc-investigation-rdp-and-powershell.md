# Day 80 – Wazuh SOC Investigation: RDP and PowerShell

## What I Did

* Conducted a mini SOC investigation starting from a Windows `4625` failed-logon alert
* Investigated the authentication context and identified **Logon Type 10 / RDP**
* Correlated repeated failed authentication attempts
* Attributed the source IP to Rahul's laptop
* Verified with the user that the activity was not authorized
* Pivoted from authentication telemetry to endpoint process activity
* Identified a suspicious **Word → PowerShell** process chain
* Decoded and analyzed a PowerShell `EncodedCommand`
* Correlated the PowerShell activity with the RDP connection
* Checked for successful authentication and confirmed there was no successful logon
* Discussed appropriate containment, evidence preservation, and L2 escalation

## Investigation Flow

```text
4625 Failed Logon
       ↓
Logon Type 10 / RDP
       ↓
Repeated Attempts
       ↓
Source IP → Rahul's Laptop
       ↓
User Denies Activity
       ↓
Endpoint Telemetry
       ↓
Word → PowerShell
       ↓
EncodedCommand
       ↓
Correlated with RDP Activity
       ↓
No Successful Logon
       ↓
Containment + Evidence Preservation
       ↓
L2 Escalation
```

## What I Understood

* A failed authentication alert by itself does not necessarily indicate an attack
* Authentication events become more suspicious when combined with repeated attempts, unusual logon types, and endpoint activity
* Parent-child process relationships can reveal suspicious execution chains
* PowerShell activity needs to be investigated using the command, user, parent process, and surrounding telemetry
* An unsuccessful attack can still require investigation and escalation
* Incident response should consider containment and evidence preservation rather than immediately deleting or modifying potentially relevant evidence

## Concepts Covered

* Windows Event ID `4625`
* RDP / Logon Type `10`
* Authentication Investigation
* Source IP Attribution
* Process Trees
* Parent-Child Processes
* Word → PowerShell
* PowerShell `EncodedCommand`
* Event Correlation
* Successful vs. Failed Authentication
* Containment
* Evidence Preservation
* L2 Escalation

## Key Takeaways

* Completed a full mini SOC investigation using Wazuh and Windows endpoint telemetry
* Practiced pivoting from an authentication alert into process and PowerShell telemetry
* Learned how multiple seemingly separate events can be correlated to build an incident timeline
* Confirmed that the suspicious activity did not result in a successful authentication
* Practiced making an incident assessment and determining appropriate response actions

## Next Step

* Continue working through realistic SOC attack scenarios
* Investigate additional Windows endpoint alerts using Wazuh
* Practice building timelines, identifying attack techniques, and determining appropriate response actions
