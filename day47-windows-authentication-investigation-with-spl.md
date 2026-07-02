# Day 47 – Windows Authentication Investigation with SPL

## What I Did

- Applied Splunk Processing Language (SPL) to investigate Windows authentication events
- Focused on building investigation queries instead of memorizing SPL syntax
- Practiced selecting the appropriate SPL commands based on different investigation objectives
- Continued developing an investigation-first approach to log analysis

## Investigation Scenarios

Worked through Windows authentication investigations involving:

- Failed login attempts
- Successful logins
- Login frequency
- User account activity
- Authentication event analysis

## SPL Commands Applied

Used:

- `index`
- Field filtering
- `table`
- `stats count`
- `stats count by`
- `where`
- `sort`
- `head`
- `dedup`

to investigate authentication events and summarize log data.

## Practical Activities

- Built SPL queries for authentication investigation scenarios
- Selected relevant fields for analyzing login activity
- Investigated failed and successful authentication events
- Applied aggregation commands to summarize authentication data
- Practiced choosing the appropriate SPL approach based on the investigation objective

## What I Understood

- Security investigations begin by understanding the alert before writing a search query
- Different investigation objectives may require different SPL approaches, even when analyzing the same Event ID
- Aggregation commands such as `stats` summarize data and replace individual events, making it important to use them at the appropriate stage of an investigation
- Authentication investigations involve validating alerts, identifying affected accounts, determining event frequency, and checking whether login attempts eventually succeeded

## Concepts Covered

- Windows Authentication
- Failed Login Investigation
- Successful Login Investigation
- SPL Query Construction
- Log Analysis
- Event Filtering
- SOC Investigation Workflow

## Key Takeaways

- Continued developing an investigation-first mindset rather than relying on memorized SPL queries
- Improved confidence in selecting appropriate SPL commands for authentication investigations
- Strengthened understanding of how SOC analysts investigate and interpret Windows authentication events

## Next Step

- Continue solving realistic SOC investigation scenarios involving process execution and endpoint activity using Windows Security Events
