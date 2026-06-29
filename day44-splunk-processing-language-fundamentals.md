# Day 44 – Splunk Processing Language (SPL) Fundamentals

## What I Did

- Shifted my focus from infrastructure setup to learning Splunk Processing Language (SPL)
- Practiced writing SPL queries by identifying the data to retrieve and selecting appropriate fields and commands
- Explored searching, filtering, and organizing Windows Security Events
- Continued investigating the Sysmon Operational log ingestion issue and confirmed it was related to the log ingestion pipeline rather than Sysmon itself

## SPL Fundamentals

Learned how SPL queries are built using:

- Index selection
- Field-value filtering
- Logical operators
- Pipeline commands

## Basic Search Syntax

Practiced using:

- `index`
- `EventCode`
- `host`
- `Image`

to search and filter Windows Security Events.

## Logical Operators

Learned the purpose of:

- `AND`
- `OR`
- `NOT`

and when to use them while building search queries.

## Working with Fields

Learned how to display only relevant information using:

- `table`

instead of viewing every available event field.

## Aggregation and Sorting

Practiced using:

- `stats count by`
- `sort`
- `head`

to summarize Windows event data and display the most relevant results.

## Practical Activities

- Built SPL queries manually instead of relying on pre-written searches
- Searched Windows Security Event IDs
- Filtered Process Creation events (Event ID 4688)
- Combined multiple search conditions
- Displayed selected event fields using `table`
- Summarized results using `stats count by`
- Sorted and limited search results
- Continued troubleshooting Sysmon Operational log ingestion

## What I Understood

- SPL queries begin with a question and are built around the data required to answer it
- Each command in an SPL pipeline performs a specific operation on the previous results
- Aggregation commands make large datasets easier to analyze during investigations
- Effective searches depend on understanding the available event fields
- Troubleshooting data collection is as important as analyzing the data itself

## Concepts Covered

- Splunk Processing Language (SPL)
- Event Filtering
- Logical Operators
- Field Selection
- `table`
- `stats`
- `sort`
- `head`
- Windows Security Events

## Key Takeaways

- Began writing SPL queries independently instead of relying on copied searches
- Learned how to summarize and organize Windows event data
- Improved my understanding of the thought process behind log analysis and investigations
- Identified the Sysmon issue as a log ingestion problem and decided to continue building SPL skills while revisiting the configuration later

## Next Step

- Continue learning intermediate SPL commands and apply them to Windows investigation scenarios
