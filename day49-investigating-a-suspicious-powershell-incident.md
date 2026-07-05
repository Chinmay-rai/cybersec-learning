# Day 49 – Investigating a Suspicious PowerShell Incident

## What I Did

- Investigated a realistic Windows endpoint security incident involving suspicious PowerShell execution
- Followed a SOC investigation workflow to validate the alert and analyze available evidence
- Developed multiple investigation hypotheses before reaching a conclusion
- Examined process relationships to understand how PowerShell was executed
- Evaluated the available evidence to determine the appropriate incident response

## Investigation Scenario

Worked through an endpoint investigation involving:

- Suspicious PowerShell execution
- Parent-child process analysis
- Email attachment investigation
- User verification
- Alert validation
- Incident assessment

## Investigation Workflow

Focused on answering questions such as:

- Is the alert legitimate?
- How was PowerShell executed?
- Which process launched PowerShell?
- Does the evidence support the user's explanation?
- Has the threat already been contained?
- Does the incident require escalation?

## Practical Activities

- Investigated a Microsoft Defender alert for suspicious PowerShell execution
- Developed multiple investigation hypotheses before drawing conclusions
- Validated user statements against available evidence
- Analyzed parent-child process relationships
- Correlated endpoint activity to reconstruct the incident timeline
- Assessed whether the incident required escalation or closure

## What I Understood

- Security alerts should be treated as indicators rather than proof of malicious activity
- User statements should always be validated using available evidence
- Parent-child process relationships provide important context during endpoint investigations
- Investigation conclusions should be based on multiple pieces of supporting evidence rather than a single suspicious event
- A true positive incident does not always require escalation if the threat has already been successfully contained

## Investigation Outcome

The simulated investigation concluded that the user opened a malicious email attachment which caused Microsoft Word to spawn an encoded PowerShell process.

Microsoft Defender successfully detected and terminated the PowerShell process while quarantining the malicious attachment.

No evidence of persistence, privilege escalation, lateral movement, or additional malicious activity was identified. Based on the available evidence, the incident was classified as a contained true positive and did not require further escalation.

## Concepts Covered

- PowerShell Investigation
- Parent-Child Process Analysis
- Microsoft Defender
- Alert Validation
- Incident Response
- Evidence-Based Decision Making
- SOC Investigation Workflow

## Key Takeaways

- Continued strengthening an investigation-first mindset instead of focusing solely on SPL syntax
- Improved confidence in developing and validating multiple investigation hypotheses
- Strengthened my ability to make incident response decisions based on collected evidence rather than assumptions
- Reinforced the importance of correlating alerts, user context, and endpoint activity during investigations

## Next Step

- Continue investigating realistic SOC incidents involving process execution, endpoint activity, and threat hunting while preparing to transition into hands-on SOC labs on TryHackMe
