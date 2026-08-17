# Day 70 – Wazuh Fundamentals and Initial Exploration

## What I Did

- Started systematically learning Wazuh and its internal workflow
- Studied the main Wazuh components and their roles
- Learned how endpoint events are processed and turned into alerts
- Investigated how Wazuh Decoders and Rules work together
- Traced a Windows authentication failure through the Wazuh detection process

## What I Studied

### Wazuh Components

- Wazuh Agent
- Wazuh Manager
- Wazuh Decoders
- Wazuh Rules
- Wazuh Alerts
- Wazuh Indexer
- Filebeat
- Wazuh Dashboard

### Event Processing

- Agent → Manager → Decoder → Rule → Alert
- Endpoint telemetry collection
- Event decoding
- Rule matching
- Alert generation

### Wazuh Rules & Alerts

Studied:

- Rule IDs and severity levels
- Rule conditions
- `if_sid` and rule chaining
- Event-field matching
- Regex matching
- Rule groups
- MITRE ATT&CK mappings
- Alert structure and important fields

## Practical Investigation

- Traced Windows Event ID `4625`
- Located Wazuh Rule `60122`
- Analyzed Rule `60122` in `0580-win-security_rules.xml`
- Understood how Rule `60105` leads to Rule `60122`
- Connected the rule configuration to the authentication-failure alert observed in the Wazuh Dashboard

## What I Understood

- Wazuh uses Decoders to interpret events and Rules to determine whether they should generate alerts
- Rules can be chained together to create more specific detections
- Alert severity does not automatically mean that an event is malicious
- Understanding the rule behind an alert provides useful investigation context

## Concepts Covered

- Wazuh Architecture
- Wazuh Agent
- Wazuh Manager
- Decoders
- Detection Rules
- Alert Generation
- Rule Chaining

## Key Takeaways

- Gained a better understanding of how Wazuh processes events and generates alerts
- Learned how to trace an alert back to the rule responsible for detecting it
- Started understanding Wazuh from a detection and investigation perspective

## Next Step

- Study the Wazuh Agent in greater depth
- Learn about Windows telemetry collection
- Explore `ossec.conf`
- Understand Agent-to-Manager communication
