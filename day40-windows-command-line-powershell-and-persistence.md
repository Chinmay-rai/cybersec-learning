# Day 40 – Windows Command Line, PowerShell, and Persistence

## What I Did

- Learned how administrators and attackers interact with Windows through command-line tools
- Reviewed the role of Command Prompt (CMD) in system administration and troubleshooting
- Explored PowerShell and its capabilities for automation and scripting
- Investigated common Windows persistence mechanisms
- Examined how services and scheduled tasks can be used to maintain persistence across system reboots

## Command-Line Tools

### Command Prompt (CMD)

Reviewed the role of CMD as the traditional Windows command-line interface.

Learned how command-line activity can be relevant during security investigations and system administration tasks.

### PowerShell

Explored PowerShell and learned how it differs from CMD.

Studied:

- Automation
- Scripting
- System Administration
- Command Execution

Learned why PowerShell is commonly used by both administrators and attackers and why monitoring PowerShell activity is important during investigations.

## Windows Services

Reviewed how Windows services operate in the background.

Explored service management using:

- `services.msc`

Learned how services can be abused to establish persistence on a system.

## Scheduled Tasks

Explored Task Scheduler using:

- `taskschd.msc`

Learned how tasks can be configured to execute:

- At startup
- At logon
- At scheduled times

Studied how scheduled tasks can be used as a persistence mechanism.

## Persistence Mechanisms

Learned the concept of persistence and its importance in cybersecurity.

Explored common persistence locations:

- Windows Services
- Scheduled Tasks
- Startup Folder
- Registry Run Keys

## What I Understood

- CMD provides basic command-line functionality while PowerShell offers advanced automation capabilities
- PowerShell is a legitimate administrative tool but is frequently abused by attackers
- Persistence mechanisms allow programs to survive system reboots
- Services and scheduled tasks are commonly examined during security investigations
- Security analysts investigate both execution activity and persistence mechanisms

## Concepts Covered

- Command Prompt (CMD)
- PowerShell
- Windows Services
- Scheduled Tasks
- Persistence
- Startup Folder
- Registry Run Keys
- Service Management
- Task Scheduler

## Key Takeaways

- Learned how administrators and attackers interact with Windows through command-line tools
- Explored common Windows persistence mechanisms
- Improved understanding of how malicious software can maintain access to a system
- Studied locations commonly investigated during incident response and threat hunting

## Tools Explored

- CMD
- PowerShell
- services.msc
- taskschd.msc

## Next Step

- Learn Sysmon and begin collecting Windows logs for analysis in Splunk
