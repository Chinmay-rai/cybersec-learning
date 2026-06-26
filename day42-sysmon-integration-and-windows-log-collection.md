# Day 42 – Sysmon Integration and Windows Log Collection

## What I Did

- Learned how Windows endpoint telemetry is collected and forwarded to SIEM platforms
- Installed the Splunk Add-on for Microsoft Windows
- Verified that Sysmon was correctly installed and generating endpoint events
- Explored the Windows Event Log collection process in Splunk
- Investigated why Sysmon events were not appearing in Splunk
- Identified that the remaining issue was related to log ingestion rather than Sysmon configuration

## Windows Log Collection

Studied:

- Windows Event Log ingestion
- Sysmon Operational logs
- Splunk Add-on for Microsoft Windows
- Splunk Data Inputs
- Local Event Log collection

## Sysmon Investigation

Generated and analyzed:

- Process Creation (Event ID 1)
- Parent-child process relationships
- Command-line information
- User context
- Process hashes

Generated endpoint activity using:

- Notepad
- Command Prompt (CMD)
- PowerShell

## Splunk

Explored:

- Windows Event Log collection workflow
- Local Event Log configuration
- Troubleshooting Windows log ingestion
- SIEM log collection architecture

## Practical Activities

- Installed the Splunk Add-on for Microsoft Windows
- Verified that the Sysmon service was running correctly
- Generated endpoint activity using Notepad, CMD, and PowerShell
- Investigated Sysmon Process Creation events through Event Viewer
- Configured Splunk to collect Windows Event Logs
- Attempted to ingest Sysmon Operational logs into Splunk
- Identified that the remaining issue was related to Splunk log ingestion rather than Sysmon configuration

## What I Understood

- Sysmon generates detailed endpoint telemetry beyond default Windows logging
- Sysmon stores its events within the Windows Event Log framework
- SIEM platforms require correctly configured data inputs before logs become searchable
- Log generation and log ingestion are separate stages of the monitoring pipeline
- Troubleshooting log collection is an important part of deploying and maintaining a SIEM

## Concepts Covered

- Windows Event Logs
- Sysmon
- Splunk
- Windows Log Collection
- Endpoint Telemetry
- Event ID 1
- Parent-Child Processes
- Process Investigation
- SIEM Data Collection

## Key Takeaways

- Successfully verified that Sysmon was generating endpoint telemetry through Event Viewer
- Improved understanding of Windows event collection and investigation workflows
- Learned how Windows endpoint telemetry flows from Sysmon to Windows Event Logs before reaching a SIEM
- Identified the remaining challenge as a Splunk log ingestion issue rather than a Sysmon configuration issue

## Next Step

- Complete Sysmon log ingestion into Splunk and begin investigating Windows endpoint activity using SPL
