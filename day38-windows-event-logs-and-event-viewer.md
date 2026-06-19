# Day 38 – Windows Event Logs and Event Viewer

## What I Did

- Learned how Windows records system and security-related activities through logs
- Explored Windows Event Viewer and navigated different log categories
- Investigated authentication-related events in the Security log
- Analyzed successful and failed logon events from my system
- Learned how security analysts use logs during investigations

## Windows Logs

Studied the purpose of Windows logs and learned how Windows continuously records important system and security activities.

Explored the following log categories:

- Application
- Security
- System
- Setup
- Forwarded Events

## Events and Event IDs

Learned that:

- An event is a single recorded activity
- Event IDs are numeric identifiers used to categorize events
- Analysts use Event IDs to quickly identify specific types of activity

## Security Log Analysis

Focused on the Security log and investigated:

- Event ID 4624 (Successful Logon)
- Event ID 4625 (Failed Logon)

Examined:

- Account Name
- Logon Type
- Failure Reason
- Status Codes
- Sub Status Codes

## Logon Types

Learned that the same Event ID can represent different scenarios depending on the Logon Type.

Examples explored:

- Interactive Logons
- Network Logons
- Service Logons
- Remote Desktop Logons

## Event Investigation

Analyzed authentication events generated on my system.

Investigated:

- Machine account activity 
- Failed logon attempts
- Status Code: 0xC000006D
- Sub Status Code: 0xC0000380

## What I Understood

- Event Viewer is used to view logs but does not generate them
- Event IDs alone are not sufficient during investigations
- Context such as account name, logon type, timestamp, and failure reason is important
- Security logs act as evidence during investigations and incident analysis

## Concepts Covered

- Windows Event Logs
- Event Viewer
- Event IDs
- Security Logs
- Authentication Events
- Event ID 4624
- Event ID 4625
- Logon Types
- Event Analysis

## Key Takeaways

- Learned how Windows records authentication and security-related events
- Gained experience analyzing real log events from my system
- Improved understanding of how security analysts investigate user activity through logs
- Built foundational knowledge for Windows-based security monitoring

## Next Step

- Learn Process Creation Events (4688) and understand how Windows records process execution activity
