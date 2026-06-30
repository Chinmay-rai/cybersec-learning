# Day 45 – SPL Investigation Practice and SOC Scenarios

## What I Did

- Strengthened my Splunk Processing Language (SPL) skills by solving SOC-style investigation scenarios
- Built SPL queries independently instead of relying on pre-written searches
- Investigated Windows Security Events using different Event IDs
- Applied previously learned SPL commands to answer investigation questions

## Investigation Scenarios

Worked with:

- Windows Security Event ID 4688 (Process Creation)
- Windows Security Event ID 4624 (Successful Logon)

Built searches to investigate:

- PowerShell execution
- Command Prompt (CMD) execution
- Notepad execution
- Multiple suspicious processes
- Successful logons
- Process execution counts

## SPL Commands Used

Applied:

- `table`
- `stats count`
- `stats count by`
- `sort`
- `head`

to organize, summarize, and analyze investigation results.

## Investigation Workflow

Focused on understanding the investigation process before writing queries.

Approached each scenario by asking:

- What happened?
- Who performed the action?
- When did it occur?
- Which host was involved?
- What command was executed?
- What process launched it?

## Practical Activities

- Wrote SPL queries without relying on copied examples
- Selected relevant fields such as `_time`, `host`, `Image`, `CommandLine`, and `Account_Name`
- Solved multiple SOC-style investigation exercises
- Chose appropriate Event IDs based on the investigation scenario

## What I Understood

- Effective SPL begins with understanding the investigation objective
- Different investigation questions require different event fields and search strategies
- Building queries independently strengthens analytical thinking more than memorizing syntax
- Investigation workflows are driven by questions rather than commands

## Concepts Covered

- Splunk Processing Language (SPL)
- Windows Security Events
- Process Creation Analysis
- Event Filtering
- Log Investigation
- SOC Workflow
- Incident Analysis

## Key Takeaways

- Improved confidence in writing SPL queries independently
- Strengthened the ability to translate investigation requirements into SPL searches
- Continued developing an investigation-first approach to log analysis

## Next Step

- Learn additional SPL commands such as `top`, `dedup`, `where`, `fields`, and `eval`, and continue solving more advanced SOC investigation scenarios
