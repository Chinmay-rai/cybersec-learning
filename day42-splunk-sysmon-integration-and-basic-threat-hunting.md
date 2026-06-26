# Day 42 – Splunk Sysmon Integration and Basic Threat Hunting

## What I Did

- Integrated Windows Sysmon logs with Splunk for centralized log analysis
- Configured Splunk to ingest Windows Event Logs and Sysmon Operational logs
- Verified successful collection and indexing of Windows endpoint events
- Generated endpoint activity using Windows applications and analyzed the resulting logs
- Used SPL to investigate process activity and user actions

## Windows Log Collection

Learned how Splunk collects and indexes Windows Event Logs.

Studied:

- Windows Event Log ingestion
- Sysmon log integration
- Splunk Add-on for Microsoft Windows
- Data Inputs and Event Collection

## Searching with SPL

Practiced searching and filtering Sysmon events using SPL.

Performed searches based on:

- Process Name
- User
- Event ID
- Process Creation Events

## Threat Hunting

Investigated:

- Process creation events
- Parent-child process relationships
- PowerShell execution
- Command Prompt execution
- Notepad execution

Learned how endpoint telemetry can be used to reconstruct user activity and investigate system behavior.

## Practical Activities

- Configured Splunk to ingest Sysmon logs
- Verified Windows events were successfully indexed
- Generated endpoint activity using Notepad, CMD, and PowerShell
- Queried events using SPL
- Performed a basic SOC-style investigation

## What I Understood

- SIEM platforms centralize endpoint logs for efficient analysis
- Sysmon provides detailed endpoint telemetry beyond default Windows logging
- SPL enables fast searching and filtering of Windows events
- Process trees, command lines, hashes, and user context help analysts investigate system activity

## Concepts Covered

- Windows Event Logs
- Sysmon
- Splunk
- SPL
- Windows Log Collection
- Endpoint Telemetry
- Threat Hunting
- Process Investigation

## Key Takeaways

- Successfully integrated Sysmon logs with Splunk
- Performed basic threat hunting using real Windows endpoint telemetry
- Improved understanding of Windows event collection and investigation workflows
- Connected Windows monitoring and SIEM concepts through hands-on practice

## Next Step

- Build detection searches, dashboards, and alerts using Windows and Sysmon logs
