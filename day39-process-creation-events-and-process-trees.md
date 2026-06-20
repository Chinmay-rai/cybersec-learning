# Day 39 – Process Creation Events and Process Trees

## What I Did

- Learned how Windows records process execution activity
- Studied Process Creation Events (Event ID 4688)
- Explored parent-child process relationships
- Learned how process trees are used during security investigations
- Investigated process creation events through Windows Event Viewer
- Examined key fields recorded within process creation events

## Process Creation Events

Learned that:

- Every running application in Windows is represented as a process
- Windows can record when a new process starts
- Event ID 4688 is used to log process creation activity

Studied how process creation logs help investigators determine:

- What process was executed
- Who executed it
- When it was executed
- What process launched it

## Parent and Child Processes

Learned that most processes are launched by another process.

Studied the concepts of:

- Parent Process
- Child Process

Examples explored:

- explorer.exe → chrome.exe
- explorer.exe → cmd.exe
- cmd.exe → powershell.exe

## Process Trees

Learned that a process tree is a chain of parent-child relationships between processes.

Explored how process trees help analysts:

- Reconstruct system activity
- Trace execution paths
- Understand process relationships
- Investigate suspicious behavior

## Common Windows Processes

Studied the purpose and security relevance of:

- explorer.exe
- cmd.exe
- powershell.exe
- conhost.exe
- svchost.exe
- rundll32.exe

## Practical Activities

- Accessed Windows Security Logs through Event Viewer
- Investigated Process Creation Events (Event ID 4688)
- Examined key event fields, including:
  - New Process Name
  - Parent Process
  - User Account
  - Timestamp
- Analyzed parent-child process relationships
- Studied examples of normal and potentially suspicious process execution chains

## What I Understood

- Process creation events provide valuable visibility into system activity
- Parent-child process relationships provide important investigation context
- Process trees help analysts understand how programs were launched
- Event IDs alone are not enough; context is essential during investigations
- Understanding normal process behavior is important for identifying suspicious activity

## Concepts Covered

- Process Creation Events
- Event ID 4688
- Process Trees
- Parent Processes
- Child Processes
- Windows Security Logs
- Event Viewer
- Process Investigation

## Key Takeaways

- Event ID 4688 records the creation of new processes
- Process trees help analysts trace execution paths and system activity
- Process creation logs are one of the most valuable sources of evidence during endpoint investigations
- Security analysts use process creation events to understand what executed, who executed it, and how it was launched

## Next Step

- Investigate additional Windows security events and continue analyzing process activity through Event Viewer
