# Day 32 – Splunk Forwarder and Log Ingestion

## What I Did

- Installed and configured Splunk Universal Forwarder on Kali Linux
- Configured Splunk Enterprise to receive forwarded data on port 9997
- Verified connectivity between the forwarder and Splunk server
- Added monitored log sources on Kali Linux
- Validated successful log ingestion into Splunk
- Explored incoming events through the Search & Reporting application

## Splunk Data Collection

Learned how Splunk collects data using forwarders and sends it to a central Splunk instance.

Studied:

- Splunk Universal Forwarder
- Receiving data on Splunk Enterprise
- Monitored inputs
- Log forwarding
- Centralized log collection

## What I Understood

- Splunk Universal Forwarder is a lightweight agent used to collect and send logs
- Splunk Enterprise can act as a central location for storing and searching log data
- Forwarded logs are automatically ingested and indexed by Splunk
- Continuous log forwarding is different from manually uploading log files
- Centralized logging makes monitoring and analysis more efficient

## Concepts Covered

- Splunk Enterprise
- Splunk Universal Forwarder
- Log Forwarding
- Data Ingestion
- Monitored Inputs
- Centralized Logging
- Search & Reporting

## Key Takeaways

- Splunk can continuously collect logs from remote systems using forwarders
- Automated log collection is more practical than manual log uploads
- Centralized logging forms the foundation of SIEM platforms
- Building a small homelab helps in understanding how logs move through a monitoring environment

## Next Step

- Learn more SPL commands and practice searching and analyzing ingested log data
