# FutureInterns Cyber Security Task 1

## Objective
Perform a basic vulnerability assessment on a publicly accessible web application using passive and non-intrusive security testing techniques.

## Target
scanme.nmap.org

## Tools Used
- Nmap
- OWASP ZAP
- SecurityHeaders.com

## Methodology

### 1. Reconnaissance
- Identified open ports and exposed services using Nmap.
- Enumerated publicly accessible network services.

### 2. Passive Vulnerability Assessment
- Conducted passive scanning using OWASP ZAP.
- Reviewed HTTP response headers.
- Analyzed security configurations.

### 3. Security Header Assessment
- Evaluated security headers using SecurityHeaders.com.

## Findings

| Finding | Severity |
|----------|----------|
| Missing Content Security Policy (CSP) | Medium |
| Missing Anti-Clickjacking Header | Medium |
| Missing Subresource Integrity (SRI) | Medium |
| Session ID Exposure in URL | Medium |
| Cross-Domain Misconfiguration | Medium |
| HTTP Exposure (No HTTPS Redirect) | Medium |
| Server Version Disclosure | Low |
| Absence of Anti-CSRF Tokens | Low |

## Nmap Results

Open Ports:
- 22/tcp (SSH)
- 80/tcp (HTTP)
- 9929/tcp (Nping Echo)
- 31337/tcp (Elite)

Filtered Ports:
- 25/tcp
- 135/tcp
- 139/tcp
- 445/tcp

## Security Headers Assessment

SecurityHeaders Grade: F

Missing Headers:
- Content-Security-Policy
- X-Frame-Options
- X-Content-Type-Options
- Referrer-Policy
- Permissions-Policy

## Recommendations

- Implement Content Security Policy (CSP).
- Enable X-Frame-Options to prevent clickjacking.
- Use Subresource Integrity (SRI) for external scripts.
- Enforce HTTPS redirection.
- Hide unnecessary server version information.
- Implement anti-CSRF protections where applicable.
- Review CORS configuration.

## Disclaimer

This assessment was conducted using passive and non-intrusive techniques only.

No exploitation, brute force, privilege escalation, or destructive testing was performed.

## Author

Pratyush Singh Rathore
Future Interns Cyber Security Internship
