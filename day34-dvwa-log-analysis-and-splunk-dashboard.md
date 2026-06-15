# Day 34 – DVWA Log Analysis and Splunk Dashboard Creation

## What I Did

- Verified that Apache access logs from the Kali Linux VM were being forwarded to Splunk Enterprise
- Generated web traffic by interacting with DVWA and confirmed that the activity appeared in Splunk
- Examined raw Apache access log events within Splunk
- Used SPL to extract useful information from web server logs

### Traffic Attributes Analyzed

- Client IP Address
- HTTP Method
- Requested URI
- HTTP Status Code

## Log Analysis

Analyzed DVWA web traffic and observed:

- Login requests
- Visits to vulnerability pages
- HTTP GET requests
- HTTP POST requests
- HTTP status codes such as 200 and 302

Used SPL searches to transform raw log events into structured data for analysis.

## Dashboard Creation

Created a dashboard containing:

- Total Request Count
- HTTP Status Code Distribution
- Most Visited Pages

Used visualizations to summarize activity generated while interacting with DVWA.

## What I Understood

- Raw logs often require field extraction before meaningful analysis can be performed
- Apache access logs contain information about user and application activity
- SPL can be used to extract and analyze data from log events
- Dashboards provide a visual way to monitor and understand log data

## Concepts Covered

- Splunk Dashboards
- Apache Access Logs
- SPL Field Extraction
- Web Traffic Analysis
- HTTP Methods
- HTTP Status Codes
- DVWA Monitoring
- Data Visualization

## Key Takeaways

- Successfully collected and analyzed DVWA-generated traffic in Splunk
- Performed basic web traffic analysis using SPL
- Created visualizations from log data using Splunk dashboards
- Gained additional hands-on experience working with real log data

## Next Step

- Continue learning SPL and perform deeper analysis of DVWA-generated events
