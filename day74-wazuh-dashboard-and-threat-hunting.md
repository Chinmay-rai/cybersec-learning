# Day 74 – Wazuh Dashboard and Threat Hunting

## What I Did

* Explored the Wazuh Dashboard as a tool for searching and investigating security events
* Practiced using searches, filters, and event fields to narrow down relevant activity
* Reviewed how severity levels should be interpreted during investigations
* Investigated activity from a specific Windows endpoint
* Used the Dashboard to investigate a Windows authentication failure

## What I Studied

### Wazuh Dashboard

* Searching and filtering security events
* Working with structured event fields
* Investigating specific agents
* Understanding alert severity
* Basic threat hunting workflow

### Important Fields

Reviewed fields such as:

* Agent
* Event ID
* Rule ID
* Severity

Also reinforced that **alert severity indicates the importance of an event but does not automatically mean the activity is malicious**.

## Practical Work

* Investigated `SOC-WIN01` through the Wazuh Dashboard
* Generated and investigated a Windows Event ID `4625` failed-logon event
* Used Dashboard filters to isolate the specific event
* Traced the event through:

```text
Agent
  ↓
Event ID
  ↓
Decoder
  ↓
Rule
  ↓
Severity
  ↓
Alert
```

## What I Understood

* The Wazuh Dashboard provides a centralized interface for searching and investigating security data
* Effective threat hunting depends on narrowing large amounts of telemetry using fields and filters
* An alert needs to be investigated in context rather than judged only by its severity

## Concepts Covered

* Wazuh Dashboard
* Search & Filtering
* Event Fields
* Alert Severity
* Agent Investigation
* Threat Hunting
* Windows Authentication Events
* Event ID `4625`

## Key Takeaways

* Became more comfortable navigating and investigating events through the Wazuh Dashboard
* Practiced filtering endpoint activity to isolate relevant security events
* Reinforced the process of moving from an alert to its underlying event and detection context

## Next Step

* Study Windows Security Logs and authentication investigation
* Investigate process monitoring and parent-child process relationships
* Learn how to identify suspicious process execution
