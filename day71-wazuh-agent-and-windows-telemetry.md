# Day 71 – Wazuh Agent and Windows Telemetry

## What I Did

- Studied the Wazuh Agent and its role as an endpoint security sensor
- Learned how the Agent collects and forwards Windows telemetry to the Wazuh Manager
- Explored Windows Event Channels and the Application, Security, and System logs
- Reviewed Event ID 4625 as an example of a failed authentication event
- Inspected the Wazuh Agent configuration file (`ossec.conf`)
- Learned how the Agent communicates and authenticates with the Wazuh Manager
- Studied how the Agent buffers events when the Manager is temporarily unavailable
- Explored the main Wazuh Agent modules used for endpoint monitoring

## Windows Telemetry

Studied:

- Windows Event Channels
- Application Logs
- Security Logs
- System Logs
- Event ID 4625
- Event Filtering

## Agent Configuration

Explored `ossec.conf` and learned how it controls:

- Manager address and port
- Communication protocol
- Agent modules
- Telemetry collection
- Reconnection settings
- Event buffering

## Agent Communication

Learned about:

- Agent → Manager communication
- TCP port `1514`
- Agent registration and authentication
- AES encryption
- Reconnection handling
- Event buffering during temporary connectivity issues

## Wazuh Agent Modules

Studied:

- SCA
- FIM / Syscheck
- Syscollector
- Rootcheck
- Active Response

## Practical Work

- Inspected the actual `ossec.conf` configuration of **SOC-WIN01**
- Connected configuration settings with the behavior of the Wazuh Agent
- Reviewed how Windows events are collected and forwarded to the Wazuh Manager

## What I Understood

- The Wazuh Agent acts as the endpoint sensor responsible for collecting security telemetry
- Windows Event Logs provide important security information that can be forwarded to Wazuh
- `ossec.conf` controls how the Agent communicates with the Manager and what telemetry it collects
- Agent buffering helps prevent events from being immediately lost during temporary Manager connectivity issues
- Different Agent modules provide visibility into different aspects of endpoint security

## Concepts Covered

- Wazuh Agent
- Windows Event Logs
- Windows Event Channels
- `ossec.conf`
- Agent Communication
- Agent Registration
- Event Buffering
- SCA
- File Integrity Monitoring
- Syscollector
- Rootcheck
- Active Response

## Key Takeaways

- Gained a deeper understanding of how the Wazuh Agent collects and forwards endpoint telemetry
- Learned how Agent configuration affects monitoring and communication
- Connected the Wazuh Agent configuration directly to the behavior of my Windows endpoint
- Improved my understanding of the endpoint side of the Wazuh monitoring pipeline

## Next Step

- Study the Wazuh Manager and its role in the event-processing pipeline
- Explore the `/var/ossec/` directory structure
- Learn about important Wazuh Manager processes
- Study Wazuh Manager logs and how they can be used for troubleshooting and investigations
