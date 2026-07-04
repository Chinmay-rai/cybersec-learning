# Day 48 – Windows Authentication Incident Investigation

## What I Did

- Investigated a realistic Windows authentication incident using a SOC investigation workflow
- Practiced validating security alerts before assuming malicious activity
- Developed multiple investigation hypotheses based on available evidence
- Applied SPL to support the investigation rather than focusing on learning new syntax
- Reconstructed an authentication timeline using Windows Security Events

## Investigation Scenario

Worked through an authentication-related investigation involving:

- Failed logon attempts
- Successful logons
- Authentication timeline analysis
- Alert validation
- User verification
- Incident hypothesis development

## SPL Applied

Used:

- `index`
- Field filtering
- `head`
- `table`

to support the investigation and analyze authentication events.

## Investigation Workflow

Focused on answering questions such as:

- Is the alert legitimate?
- Who generated the authentication events?
- Did the failed logins eventually succeed?
- Does the activity appear normal or suspicious?
- What additional information would help validate the alert?

## What I Understood

- Security alerts indicate suspicious activity but do not confirm malicious behavior
- User-reported incidents should be validated using log evidence before drawing conclusions
- Multiple failed logins followed by a successful login may represent either legitimate user activity or malicious behavior depending on the surrounding context
- Effective investigations require continuously updating hypotheses as new evidence becomes available
- SOC investigations often involve communicating with users and the Help Desk in addition to analyzing logs

## Concepts Covered

- Windows Authentication
- Alert Validation
- Authentication Timeline Analysis
- Incident Response
- Hypothesis-Based Investigation
- SOC Investigation Workflow

## Key Takeaways

- Continued developing an investigation-first mindset during Windows authentication analysis
- Improved my ability to evaluate multiple explanations before reaching a conclusion
- Strengthened investigative thinking by combining log analysis with contextual information from users and the Help Desk

## Next Step

- Continue investigating realistic SOC incidents involving authentication, process execution, and endpoint activity
