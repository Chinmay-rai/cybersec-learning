# Day 76 – PowerShell Telemetry and Command Investigation

## What I Did

- Revised PowerShell telemetry and logging in Wazuh
- Reviewed how PowerShell activity is collected from Windows endpoints
- Revisited important PowerShell logging mechanisms and Event IDs
- Practiced thinking about how suspicious PowerShell activity should be investigated

## What I Studied

### PowerShell Telemetry

- PowerShell Operational Logging
- Script Block Logging
- Event ID `4104`
- Module Logging
- PowerShell event identification
- PowerShell activity collected by Wazuh

### Suspicious PowerShell Investigation

Reviewed how analysts examine:

- Commands and scripts
- User accounts
- Processes
- Parent processes
- Surrounding activity

to determine whether PowerShell execution is expected or suspicious.

## What I Understood

- PowerShell can generate different types of telemetry depending on the logging mechanisms enabled
- Script Block Logging provides important visibility into the actual PowerShell commands and scripts being executed
- Event ID `4104` is particularly useful when investigating PowerShell activity
- Suspicious PowerShell execution needs to be investigated using the command itself along with user, process, parent process, and surrounding event context

## Concepts Covered

- PowerShell Telemetry
- PowerShell Operational Logging
- Script Block Logging
- Event ID 4104
- Module Logging
- PowerShell Investigation
- Suspicious Command Analysis
- Wazuh Windows Monitoring

## Key Takeaways

- Reinforced my understanding of PowerShell telemetry in Wazuh
- Improved my understanding of how different PowerShell logging mechanisms provide investigation evidence
- Strengthened my approach to investigating suspicious PowerShell commands using multiple pieces of endpoint context

## Next Step

- Study Sysmon
- Explore process, network, and file telemetry
- Understand why Sysmon is valuable for SOC investigations
