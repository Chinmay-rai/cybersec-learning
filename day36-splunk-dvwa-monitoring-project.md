# Day 36 – Splunk DVWA Monitoring Project

## What I Did

- Continued working with my Splunk homelab consisting of Splunk Enterprise, Kali Linux, Apache, DVWA, and a Splunk Universal Forwarder

- Generated web activity by interacting with multiple DVWA vulnerability modules, including:
  - Brute Force
  - Reflected XSS
  - Stored XSS
  - SQL Injection
  - File Inclusion
  - Command Injection

- Investigated Apache access logs forwarded to Splunk from the Kali Linux VM

- Used SPL queries to analyze web application activity and log data

- Created a Splunk dashboard to monitor and visualize DVWA activity

- Completed and documented a Splunk-based DVWA monitoring project

- Published the project to a dedicated GitHub repository

## Log Analysis

Analyzed:

- Total Requests
- HTTP Methods (GET and POST)
- HTTP Status Codes
- Most Visited Pages
- Vulnerability-Related Activity

Observed how different DVWA modules generated different request patterns and response codes.

## Dashboard Creation

Created a Splunk dashboard to visualize:

- Total Request Count
- HTTP Method Distribution
- HTTP Status Code Distribution
- Most Visited Pages
- Vulnerability-Related Activity

Used visualizations to monitor and analyze activity generated while interacting with DVWA.

## Project Link

- [DVWA Monitoring Project](https://github.com/Chinmay-rai/splunk-dvwa-monitoring)

## What I Understood

- Apache access logs provide valuable visibility into web application activity
- Different attack scenarios can generate distinct request patterns
- SPL can be used to identify and analyze web application activity from log data
- Dashboards help summarize and visualize large amounts of event data

## Concepts Covered

- Splunk Dashboards
- SPL
- Apache Access Logs
- Web Traffic Analysis
- HTTP Methods
- HTTP Status Codes
- DVWA Monitoring
- Log Visualization

## Key Takeaways

- Built a complete Splunk-based monitoring project using real log data
- Gained hands-on experience with log collection, analysis, and visualization
- Improved understanding of how web application activity appears in Apache logs
- Documented and published the project in a dedicated GitHub repository

## Next Step

- Begin learning Windows fundamentals for security monitoring and SOC-related investigations
