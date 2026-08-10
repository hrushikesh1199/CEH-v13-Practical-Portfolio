# Module 14 — Hacking Web Applications

## Overview
Application-layer reconnaissance and exploitation, aligned to the OWASP Top 10, covering spidering, automated scanning, brute force, and remote code execution.

## Learning Objectives
- Perform web application reconnaissance using Nmap and Telnet
- Spider/crawl an application using OWASP ZAP
- Perform automated vulnerability scanning using SmartScanner
- Perform credential brute-forcing using Burp Suite Intruder
- Exploit a Remote Code Execution (RCE) vulnerability
- Scan for vulnerabilities using N-Stalker

## Labs Completed
- Lab 1.1 — Web App Reconnaissance using Nmap and Telnet
- Lab 1.2 — Web Spidering using OWASP ZAP
- Lab 1.3 — Vulnerability Scanning using SmartScanner
- Lab 2.1 — Brute-force Attack using Burp Suite
- Lab 2.2 — Remote Code Execution (RCE) Attack
- Lab 3 — Detect Web App Vulnerabilities using N-Stalker
- Lab 4 — Web Application Hacking using ShellGPT

## Tools & Technologies
- OWASP ZAP
- Burp Suite
- SmartScanner
- N-Stalker
- Nmap

## Key Commands / Techniques
```bash
zap-cli quick-scan --self-contained -o '-config api.disablekey=true' target.com
burpsuite   # Intruder module used for credential brute-force in isolated lab
```

## Sample Payloads / Test Strings
```
id;whoami   # command-injection test payload for RCE identification (lab context)
```
> All commands and payloads above were executed strictly within EC-Council's isolated CEH iLabs cyber range against consenting lab targets, for educational and certification purposes only.

## Detection & Mitigation
- Adopt OWASP ASVS as a secure-development baseline
- Implement input validation, output encoding, and parameterized system calls
- Enforce account lockout / CAPTCHA / rate limiting to prevent brute force
- Run SAST/DAST scanning in CI/CD pipelines before production deployment
- Apply the principle of least privilege to application service accounts

## Key Definitions
| Term | Definition |
|---|---|
| **RCE** | Remote Code Execution — a vulnerability class allowing an attacker to execute arbitrary code on a target system. |
| **Spidering/Crawling** | Automated discovery of an application's pages, parameters, and endpoints. |
| **OWASP Top 10** | The industry-standard awareness list of the ten most critical web application security risks. |

## References / Sources
- OWASP Top 10 — https://owasp.org/www-project-top-ten/
- OWASP ASVS — https://owasp.org/www-project-application-security-verification-standard/
- EC-Council CEH v13 Module 14

---
[⬅ Back to main README](../../README.md)
