# Day 31 – Splunk Fundamentals and Initial Exploration

## What I Did

- Installed Splunk Enterprise and completed the initial setup
- Explored the Splunk web interface and Search & Reporting application
- Learned the basic purpose of SIEM platforms and how Splunk is used for log analysis
- Investigated Splunk's internal log data using search queries

## Core Splunk Concepts

Studied:

- Events
- Indexes
- Hosts
- Sources

Learned how Splunk stores, organizes, and searches machine-generated data.

## Search Processing Language (SPL)

Practiced basic SPL queries, including:

- Viewing indexed data
- Limiting search results
- Counting events
- Displaying selected fields
- Sorting search results

## Example commands explored:

- "index=_internal"
- "index=_internal | head 10"
- "index=_internal | stats count"
- "index=_internal | stats count by source"
- "index=_internal | table _time source host"
- "index=_internal | sort -_time"

## What I Understood

- Splunk collects and indexes machine-generated data for analysis
- Events are individual log records stored by Splunk
- Indexes organize data to make searches efficient
- Sources identify where log data originates
- Hosts help identify the systems associated with events
- SPL is used to search, filter, and analyze information stored in Splunk

## Concepts Covered

- SIEM Basics
- Splunk Enterprise
- Search & Reporting
- Events
- Indexes
- Hosts
- Sources
- Internal Log Analysis
- SPL Basics

## Key Takeaways

- Splunk provides a centralized platform for log analysis and monitoring
- Understanding how data is organized is important before performing investigations
- SPL is the foundation for searching and analyzing data in Splunk
- Previous Linux log analysis knowledge helps when working with Splunk

## Next Step

- Learn more SPL commands and practice log analysis in Splunk
