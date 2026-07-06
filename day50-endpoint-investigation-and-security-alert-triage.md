# Day 50 – Endpoint Investigation and Security Alert Triage

## What I Did

- Practiced triaging multiple security alerts using a SOC investigation workflow
- Prioritized alerts based on severity, potential impact, and available evidence
- Investigated a Microsoft Defender alert involving suspicious PowerShell execution
- Built an investigation timeline using alert details and user context
- Continued developing an evidence-based approach to incident response

## Investigation Scenarios

Worked through realistic endpoint investigations involving:

- Security alert triage
- Suspicious PowerShell execution
- Encoded PowerShell commands
- Parent-child process analysis
- Email attachment investigation
- Endpoint activity validation

## SPL Applied

Applied previously learned SPL concepts to support investigations, including:

- `index`
- Host filtering
- Time-based filtering (`earliest` / `latest`)
- Process-based filtering
- Event correlation

## Investigation Workflow

Focused on answering questions such as:

- Which alert should be investigated first?
- Is the alert legitimate?
- What was the initial cause of the activity?
- What impact did the activity have on the endpoint?
- Is there evidence of additional malicious behavior?
- Does the incident require escalation?

## What I Understood

- Effective SOC investigations begin with alert validation rather than assumptions
- Investigation objectives evolve as new evidence becomes available
- Once the initial cause is confirmed, investigators should focus on determining the overall impact
- Parent-child process relationships provide valuable context during endpoint investigations
- Investigation strategies should adapt based on available telemetry rather than assuming a specific log source or Event ID

## Concepts Covered

- Security Alert Triage
- Endpoint Investigation
- Parent-Child Process Analysis
- Incident Response
- Microsoft Defender
- Evidence-Based Decision Making
- SOC Investigation Workflow

## Key Takeaways

- Improved my ability to prioritize multiple SOC alerts based on risk and impact
- Strengthened analytical thinking by challenging assumptions throughout investigations
- Focused on understanding the consequences of suspicious activity instead of simply confirming that an alert occurred
- Continued developing a structured investigation methodology for endpoint security incidents

## Next Step

- Begin solving hands-on SOC investigation labs on TryHackMe while applying Windows event analysis, SPL, and incident response techniques learned throughout this learning journey
