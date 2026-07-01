# Day 46 - SPL Query construction and investigation

## What I Did

- Continued strengthening my Splunk Processing Language (SPL) skills through SOC-style investigation scenarios
- Built SPL queries independently instead of relying on pre-written examples
- Selected appropriate SPL commands based on the investigation objective
- Continued developing an investigation-first approach to log analysis

## SPL Commands Practiced

Worked with:

- `top`
- `dedup`
- `fields`
- `where`
- `head`
- `table`
- `stats count`
- `stats count by`
- `sort`

Learned when each command is most appropriate during different investigation scenarios.

## Investigation Scenarios

Applied SPL to investigate:

- Process Creation Events
- PowerShell execution
- Command Prompt (CMD) execution
- Latest user logins
- Frequently executed processes
- Parent-child process relationships
- Windows authentication events

## Practical Activities

- Built SPL queries independently for multiple investigation scenarios
- Selected the appropriate SPL command based on the investigation question
- Distinguished between event searches and statistical analysis
- Applied different commands to organize, summarize, and filter investigation results

## What I Understood

- Different SPL commands solve different investigation problems, even when they produce similar-looking results
- `head`, `dedup`, and `top` each have specific use cases during investigations
- `fields` can be used to keep or remove fields before continuing a search
- `where` provides additional filtering after search results have been processed
- Effective investigations begin with understanding the objective before constructing SPL queries

## Concepts Covered

- Splunk Processing Language (SPL)
- Windows Event Analysis
- Process Investigation
- Authentication Analysis
- Event Filtering
- SOC Investigation Workflow
- Threat Hunting Fundamentals

## Key Takeaways

- Improved confidence in writing SPL queries without relying on predefined examples
- Strengthened my understanding of selecting the right SPL command for different investigation objectives
- Continued shifting from memorizing commands to thinking like a SOC analyst during investigations

## Next Step

- Apply the learned SPL commands to realistic SOC investigations involving authentication attacks, suspicious process execution, privilege escalation, and endpoint activity analysis
