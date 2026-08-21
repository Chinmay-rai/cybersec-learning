# Day 73 – Wazuh Event Processing and Rule Chaining

## What I Did

* Studied how Wazuh processes raw events and converts them into security alerts
* Learned how Decoders extract information from incoming events
* Explored how Wazuh Rules evaluate decoded event fields
* Studied rule chaining and how multiple rules can work together
* Traced a Windows authentication failure through the Wazuh detection pipeline

## Wazuh Event Processing

Learned the basic processing flow:

```text
Raw Event
    ↓
Decoder
    ↓
Rule Matching
    ↓
Alert
```

Understood how Wazuh transforms raw event data into structured information that can be evaluated by detection rules.

## Decoders

Studied:

* Decoder structure
* Extracting information from events
* Creating fields for rule evaluation
* Windows decoder definitions

## Wazuh Rules

Studied:

* Rule IDs and severity levels
* Rule conditions
* `<if_sid>` and rule chaining
* `<field>` conditions
* Regex-based matching
* Rule groups
* MITRE ATT&CK mappings

## Windows Event Detection

Investigated:

* `win.system.eventID`
* Event ID `4625`
* Rule `60105` – Windows Logon Failure
* Rule `60122` – Logon Failure / Unknown User or Bad Password

## Practical Work

* Explored Windows decoder definitions
* Inspected Rules `60105` and `60122`
* Traced how Event ID `4625` passes through chained rules
* Connected the Windows event to the final Wazuh authentication-failure alert

## What I Understood

* Decoders extract and structure information from raw events
* Rules use decoded fields to identify specific activity
* Rule chaining allows Wazuh to build more specific detections from existing rules
* Understanding the processing pipeline makes it easier to investigate why a particular alert was generated

## Concepts Covered

* Wazuh Event Processing
* Decoders
* Detection Rules
* Rule Chaining
* `<if_sid>`
* `<field>`
* Regex Matching
* Windows Event Detection
* Event ID `4625`
* MITRE ATT&CK

## Key Takeaways

* Gained a deeper understanding of how Wazuh converts raw events into security alerts
* Learned how Decoders and Rules work together during event analysis
* Successfully traced a Windows authentication event through chained Wazuh rules
* Improved my understanding of how Wazuh detection logic works behind the Dashboard

## Next Step

* Explore Wazuh Dashboard and Threat Hunting
* Practice searches, filters, fields, severity, and agent-based analysis
