# Day 37 – Windows Processes, Services, and User Information

## What I Did

- Started learning Windows fundamentals
- Learned the difference between processes, threads, and services
- Explored running processes using Windows command-line tools
- Investigated several important Windows processes and their functions
- Examined Windows services using the Services management console
- Explored user and system information using built-in Windows commands

## Process Investigation

Studied the purpose of the following Windows processes:

- explorer.exe
- svchost.exe
- winlogon.exe
- lsass.exe

Learned how these processes contribute to normal system operation and why they are relevant during security investigations.

## User and System Information

Examined:

- Current user identity
- Hostname information
- Windows privileges

Used command-line tools to understand how user and system information can be collected during investigations.

## Commands Practiced

- `tasklist`
- `tasklist /svc`
- `tasklist | findstr explorer`
- `tasklist | findstr lsass`
- `tasklist | findstr svchost`
- `tasklist | findstr winlogon`
- `whoami`
- `whoami /priv`
- `hostname`

## What I Understood

- Processes, threads, and services serve different roles within Windows
- Several Windows processes are critical for authentication, logon, and system functionality
- User and privilege information can be collected using built-in Windows commands
- Understanding normal system activity is important when identifying suspicious behavior
- Establishing a baseline of legitimate processes helps during security investigations

## Concepts Covered

- Processes
- Threads
- Services
- Windows Process Investigation
- Windows Services
- User Identity
- Windows Privileges
- Host Information
- Basic SOC Investigation Concepts

## Key Takeaways

- Learned how to inspect processes and services in Windows
- Explored user and privilege information using command-line tools
- Studied important Windows processes commonly encountered during investigations
- Began building Windows knowledge relevant to SOC and security monitoring

## Next Step

- Continue learning Windows administration and system monitoring fundamentals
