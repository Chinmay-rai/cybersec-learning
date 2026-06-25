# Day 41 – Sysmon Endpoint Monitoring and Event Logging

## What I Did

- Learned about Sysmon (System Monitor) and its role in Windows endpoint monitoring
- Explored how Sysmon extends the default Windows logging capabilities
- Studied the Sysmon architecture, including its service and driver
- Installed Sysmon on Windows and verified the installation
- Examined Sysmon Operational logs using Windows Event Viewer
- Compared Sysmon-generated events with default Windows Event Logs

## Sysmon Fundamentals

Learned:

- Purpose of Sysmon
- Difference between Windows Event Logs and Sysmon
- How Sysmon improves endpoint visibility
- Integration with Windows Event Viewer

## Important Sysmon Events

Studied the following Sysmon Event IDs:

- Event ID 1 – Process Creation
- Event ID 3 – Network Connection
- Event ID 11 – File Creation
- Event ID 13 – Registry Value Set

Learned how these events provide detailed telemetry that can be used during security investigations.

## Practical Activities

- Installed Sysmon on Windows
- Verified the Sysmon service was running
- Explored the Sysmon Operational log in Event Viewer
- Observed how Sysmon records endpoint activity
- Compared Sysmon logs with default Windows logging

## What I Understood

- Sysmon significantly enhances Windows endpoint visibility
- Sysmon records detailed information about processes, network connections, file creation, and registry changes
- Endpoint telemetry collected by Sysmon is valuable during threat detection and incident investigations
- Sysmon logs can be forwarded to SIEM platforms for centralized monitoring and analysis

## Concepts Covered

- Sysmon
- Endpoint Monitoring
- Windows Event Logs
- Sysmon Operational Log
- Process Creation
- Network Connections
- File Creation
- Registry Monitoring
- Event Viewer

## Key Takeaways

- Installed and configured Sysmon for endpoint monitoring
- Learned how Sysmon extends the default Windows logging capabilities
- Explored key Sysmon event types used during investigations
- Built a foundation for collecting and analyzing Windows endpoint telemetry in a SIEM

## Next Step

- Integrate Sysmon logs with Splunk and perform basic threat hunting using real endpoint telemetry
