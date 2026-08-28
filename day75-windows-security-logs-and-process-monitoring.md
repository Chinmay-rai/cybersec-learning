# Day 75 – Windows Security Logs and Process Monitoring

## What I Did

- Studied Windows Security Logs and how they are used for security investigations in Wazuh
- Reviewed important Windows authentication events
- Learned how process creation events provide visibility into endpoint activity
- Studied parent-child process relationships and execution chains
- Learned how to identify potentially suspicious process execution using surrounding context

## What I Studied

### Windows Security Logs

- Authentication and security-related events
- Event ID `4624` – Successful Logon
- Event ID `4625` – Failed Logon
- Event ID `4634` – Logoff
- Event ID `4648` – Explicit Credential Logon

### Authentication Investigation

Studied how analysts use fields such as:

- Username
- Logon Type
- Source IP
- Process
- Authentication Package

to investigate authentication activity and determine whether it is expected or suspicious.

### Process Monitoring

- Event ID `4688` – Process Creation
- Process execution activity
- Parent-child process relationships
- Process execution chains

### Suspicious Process Execution

Learned how analysts examine:

- Process
- Parent Process
- Command Line
- User
- Surrounding Events

to identify potentially suspicious execution and understand the context behind an event.

## What I Understood

- Windows Security Logs provide valuable evidence for authentication and endpoint investigations
- Authentication events need to be examined using their surrounding context rather than Event IDs alone
- Parent-child process relationships help analysts understand how a process was launched
- Suspicious process execution is identified by combining process information with user, command line, parent process, and other surrounding activity

## Concepts Covered

- Windows Security Logs
- Authentication Events
- Event IDs 4624, 4625, 4634, 4648
- Event ID 4688
- Process Monitoring
- Parent-Child Processes
- Process Execution
- Authentication Investigation
- Suspicious Activity Analysis

## Key Takeaways

- Strengthened my understanding of Windows authentication investigation in Wazuh
- Learned how process creation and parent-child relationships provide important endpoint context
- Improved my ability to approach Windows events from an investigation perspective rather than relying only on individual Event IDs

## Next Step

- Continue investigating Windows endpoint activity in Wazuh
- Analyze authentication and process events together
- Begin working through more realistic SOC investigation scenarios
