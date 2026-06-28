# Day 43 – Windows Security Log Forwarding with Splunk Universal Forwarder

## What I Did

- Installed Splunk Universal Forwarder on Windows
- Connected the Universal Forwarder to Splunk Enterprise
- Configured Windows Event Log inputs for log forwarding
- Enabled Windows Process Creation auditing
- Verified successful forwarding of Windows Security Event Logs to Splunk
- Continued troubleshooting Sysmon Operational log forwarding

## Windows Event Collection

Configured Splunk to collect the following Windows Event Logs:

- Security
- System
- Application

Verified that Windows Security events were successfully indexed and searchable using SPL.

## Security Event IDs Verified

Investigated the following Windows Security Event IDs:

- Event ID 4624 – Successful Logon
- Event ID 4634 – Logoff
- Event ID 4648 – Logon Using Explicit Credentials
- Event ID 4672 – Special Privileges Assigned
- Event ID 4688 – Process Creation

## Practical Activities

- Installed and configured Splunk Universal Forwarder
- Connected the forwarder to Splunk Enterprise on port 9997
- Created Windows Event Log inputs
- Enabled Process Creation auditing through Local Security Policy
- Generated endpoint activity using Notepad, Command Prompt, and PowerShell
- Verified Windows Security Event forwarding through SPL
- Investigated Sysmon Operational log forwarding

## What I Understood

- Universal Forwarder collects and forwards Windows Event Logs to Splunk
- Windows Security auditing and Sysmon provide different types of endpoint telemetry
- Process Creation auditing (Event ID 4688) is an important source of investigation data
- Windows Event forwarding requires correctly configured log inputs
- Troubleshooting log collection is an essential part of deploying a SIEM

## Concepts Covered

- Splunk Universal Forwarder
- Splunk Enterprise
- Windows Event Logs
- Windows Security Auditing
- Event ID 4688
- SPL
- Windows Log Forwarding
- SIEM Data Collection

## Key Takeaways

- Successfully built a Windows-to-Splunk log forwarding pipeline using Splunk Universal Forwarder
- Verified successful ingestion of multiple Windows Security Event IDs
- Enabled Windows Process Creation auditing for endpoint monitoring
- Isolated the remaining issue to the Sysmon Operational log channel rather than the forwarding pipeline

## Next Step

- Complete Sysmon Operational log ingestion into Splunk and begin investigating Windows endpoint activity using Sysmon telemetry and SPL
