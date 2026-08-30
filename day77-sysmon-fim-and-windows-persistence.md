# Day 77 – Sysmon, FIM and Windows Persistence

## What I Did

- Studied Sysmon and its role in endpoint monitoring
- Learned how Sysmon provides detailed process, network, and file telemetry
- Reviewed how different telemetry sources can be correlated during investigations
- Studied File Integrity Monitoring and common Windows persistence mechanisms

## What I Studied

### Sysmon

- Purpose of Sysmon
- Why SOCs use Sysmon
- Event ID `1` – Process Creation
- Event ID `3` – Network Connection
- Event ID `11` – File Creation
- Parent-child process relationships
- Correlating process, network, and file activity

### File Integrity & Persistence

- File Integrity Monitoring (FIM)
- Windows Services
- Scheduled Tasks
- Windows Registry
- Persistence mechanisms
- Detecting changes that may indicate persistence

## What I Understood

- Sysmon provides detailed endpoint telemetry that can give analysts more context than standard Windows logs
- Process, network, and file activity can be correlated to reconstruct endpoint behavior
- FIM helps detect changes to important files and configurations
- Services, Scheduled Tasks, and certain Registry locations can be abused to establish persistence
- Persistence allows malicious activity or programs to survive events such as reboots and logouts

## Concepts Covered

- Sysmon
- Process Telemetry
- Network Telemetry
- File Telemetry
- Event IDs 1, 3 and 11
- Parent-Child Processes
- File Integrity Monitoring
- Windows Services
- Scheduled Tasks
- Windows Registry
- Persistence

## Key Takeaways

- Strengthened my understanding of endpoint telemetry and how different data sources can be correlated
- Learned why Sysmon is valuable for detailed SOC investigations
- Understood how FIM and Windows persistence mechanisms fit into endpoint monitoring and threat detection

## Next Step

- Continue exploring Windows endpoint detection in Wazuh
- Start correlating Sysmon, authentication, process, and persistence-related telemetry during investigations
- Move toward more realistic SOC investigation scenarios
