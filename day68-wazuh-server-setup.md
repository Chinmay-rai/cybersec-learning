# Day 68 – Wazuh Server Setup

## What I Did

* Moved on to the security monitoring layer of my SOC lab
* Installed Wazuh on my Kubuntu host
* Set up the Wazuh Manager, Indexer, Dashboard, and Filebeat components
* Verified that the Wazuh services were running successfully
* Accessed the Wazuh Dashboard for the first time
* Identified the resource requirements of running the complete Wazuh stack alongside the Windows VM
* Planned a resource-efficient workflow for the lab

## What I Understood

* Wazuh consists of multiple components that work together to collect, process, index, and visualize security data
* The Wazuh Manager handles security analysis and alert generation
* The Indexer stores and makes collected security data searchable
* The Dashboard provides the interface for monitoring and investigating alerts
* Running a complete security monitoring stack alongside a Windows endpoint requires careful resource management

## Concepts Covered

* Wazuh Architecture
* Wazuh Manager
* Wazuh Indexer
* Wazuh Dashboard
* Filebeat
* Security Monitoring
* Alert Management
* SOC Lab Infrastructure

## Key Takeaways

* Successfully installed and initialized the Wazuh security monitoring stack
* Verified that the required Wazuh services are running
* Accessed the Wazuh Dashboard and prepared the environment for endpoint monitoring
* Gained a better understanding of the infrastructure required to build a Wazuh-based SOC lab

## Next Step

* Install and configure the Wazuh Agent on the Windows endpoint
* Establish communication between the Windows endpoint and Wazuh Manager
* Generate security activity and begin investigating Wazuh alerts
