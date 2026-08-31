# Day 78 – Wazuh Custom Rules and Event Correlation

## What I Did

- Studied how custom Wazuh detection rules are structured
- Learned how rules use conditions to identify specific security events
- Practiced field matching and rule chaining
- Learned the difference between single-event chaining and multi-event correlation
- Explored how frequency and timeframes can be used to detect repeated activity

## What I Studied

### Custom Rules

- Custom rule structure
- Rule IDs
- Severity levels
- Field matching
- Multiple conditions
- `if_sid`
- `if_matched_sid`

### Event Correlation

Learned the difference between:

- **Single-event chaining** using `if_sid`
- **Multi-event correlation** using `if_matched_sid`
- Frequency-based detection
- Timeframe-based detection

## What I Understood

- Custom rules allow Wazuh detections to be tailored to specific security requirements
- Multiple conditions can make detections more precise
- `if_sid` is useful for building detection logic based on a previously matched rule
- `if_matched_sid` can be used to correlate repeated events over a specific timeframe
- Frequency and timeframe conditions help detect patterns that cannot be identified from a single event

## Concepts Covered

- Custom Wazuh Rules
- Rule Structure
- Rule IDs
- Severity
- Field Matching
- Rule Chaining
- `if_sid`
- `if_matched_sid`
- Event Correlation
- Frequency
- Timeframe

## Key Takeaways

- Learned how custom rules can extend Wazuh's detection capabilities
- Understood the difference between chaining rules for a single event and correlating multiple events
- Built a foundation for creating more meaningful and context-aware detections

## Next Step

- Study Detection Engineering
- Learn how to tune detections and reduce false positives
- Practice designing rules based on realistic SOC detection requirements
