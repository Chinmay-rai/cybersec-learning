# Day 3 – Cookies and Sessions

## What I Did
- Learned about cookies and sessions  
- Used DVWA to observe how session IDs work  
- Used Burp Suite to intercept and modify HTTP requests  

## What I Understood
- HTTP is stateless (server does not remember user)  
- Cookies store session IDs in browser  
- Session ID represents user identity  

## Practical Work
- Intercepted requests using Burp Suite  
- Observed cookies like PHPSESSID in requests  
- Modified session ID in a request  

## Observation
- Changing session ID to an invalid value logged me out  
- This shows server relies on valid session IDs for authentication  

## Learning
- Session ID is the key to user identity  
- If an attacker gets a valid session ID, they can act as that user  

## Tools Used
- Burp Suite  
- DVWA  

## Next Step
- Start learning vulnerabilities like XSS
