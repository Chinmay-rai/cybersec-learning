# Day 35 – Splunk Investigation of DVWA Web Activity

## What I Did

- Continued working with my Splunk homelab consisting of Splunk Enterprise, Kali Linux, Apache, DVWA, and a Splunk Universal Forwarder
- Generated additional web traffic by interacting with DVWA vulnerability modules
- Performed Reflected XSS and Stored XSS testing within DVWA
- Verified that the resulting web requests were captured in Apache access logs and forwarded to Splunk

## Log Analysis

Used SPL searches to investigate activity associated with DVWA pages, including:

- Login activity
- Reflected XSS page access
- Stored XSS page access
- General web application traffic

Performed searches to identify:

- Request counts
- HTTP methods (GET and POST)
- Accessed URLs
- Request timelines

## Investigation Findings

### Reflected XSS

- Observed requests to the Reflected XSS page
- Identified that activity was primarily recorded as GET requests
- Learned that reflected payloads are commonly transmitted through URL parameters

### Stored XSS

- Observed both GET and POST requests
- Verified that payload submission generated POST requests
- Confirmed payload persistence by observing repeated page interactions after submission

## What I Understood

- Apache access logs provide visibility into user interaction with web applications
- Different web vulnerabilities can generate different request patterns
- GET and POST requests can help identify how an application is being used
- Splunk can be used to reconstruct user activity by analyzing web server logs

## Concepts Covered

- Web Log Analysis
- Apache Access Logs
- HTTP Methods
- GET Requests
- POST Requests
- Reflected XSS
- Stored XSS
- SPL Investigation Techniques

## Key Takeaways

- Successfully correlated DVWA activity with events observed in Splunk
- Used log analysis to distinguish between reflected and stored XSS interactions
- Improved understanding of how web application activity appears in log data
- Continued practicing log analysis and investigation using a cybersecurity homelab

## Next Step

- Build a small Splunk project using the collected DVWA log data
