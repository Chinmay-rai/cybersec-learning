# Day 29 – Linux Log Analysis Fundamentals

## What I Did
- Learned what system logs are and how they record events on Linux systems
- Explored logs using the `journalctl` utility
- Studied the structure of log entries, including:
  - Timestamp
  - Host
  - Source/Process
  - Event Message

### Log Exploration
Practiced viewing logs using:
- `journalctl`
- `journalctl -b`
- `journalctl -n 50`
- `journalctl -f`

### Log Filtering
- Used `grep` to filter and search log entries
- Practiced identifying relevant events from large amounts of log data

### Log Investigation
Analyzed:
- Service startup events
- Error events
- `sudo` activity logs

Investigated repeated VirtualBox-related errors and determined they were non-security-related system noise rather than indicators of malicious activity.

### Log Interpretation
Practiced answering key investigation questions:
- Who performed an action?
- What action occurred?
- When did it happen?
- Was it successful or failed?

## What I Understood
- System logs provide a record of activities and events occurring on a Linux system
- Log entries contain valuable information that can be used for troubleshooting and security monitoring
- Not every error in a log represents a security issue; understanding context is important
- Filtering and searching logs is essential when working with large amounts of log data
- Effective log analysis involves identifying who performed an action, what occurred, when it happened, and whether it succeeded or failed

## Concepts Covered
- System logs
- Log entry structure
- `journalctl`
- Log filtering
- `grep`
- Service events
- Error analysis
- `sudo` logs
- Basic log investigation

## Key Takeaways
- Logs are one of the primary sources of information for troubleshooting and security investigations
- Understanding log structure makes analysis easier and more efficient
- Context is important when distinguishing between normal system activity and potential security concerns
- Basic log analysis skills form an important foundation for SIEM and SOC-related work

## Next Step
- Begin exploring SIEM tools such as Splunk
