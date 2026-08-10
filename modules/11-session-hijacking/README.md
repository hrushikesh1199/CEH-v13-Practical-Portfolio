# Module 11 — Session Hijacking

## Overview
Techniques for taking over an authenticated session at the network or application layer, and traffic-based detection of hijacking attempts.

## Learning Objectives
- Understand session token theft/hijacking concepts
- Intercept and manipulate HTTP traffic using an interception proxy
- Detect session hijacking indicators using Wireshark

## Labs Completed
- Lab 1.1 — Session Hijacking Concepts (Caido)
- Lab 1.2 — Intercept HTTP Traffic Using Hetty
- Lab 2 — Detect Session Hijacking Using Wireshark

## Tools & Technologies
- Caido
- Hetty
- Wireshark
- Burp Suite

## Key Commands / Techniques
```bash
wireshark -Y 'http.cookie' -i eth0     # filter for session cookie exposure in cleartext
```

## Sample Payloads / Test Strings
```
N/A for this module.
```
> All commands and payloads above were executed strictly within EC-Council's isolated CEH iLabs cyber range against consenting lab targets, for educational and certification purposes only.

## Detection & Mitigation
- Use Secure, HttpOnly, and SameSite cookie flags for all session tokens
- Enforce HTTPS/TLS everywhere (HSTS) to prevent cleartext token interception
- Implement short session lifetimes with re-authentication for sensitive actions
- Bind sessions to client fingerprint attributes (IP/device) where feasible
- Regenerate session ID after login (session fixation prevention)

## Key Definitions
| Term | Definition |
|---|---|
| **Session Hijacking** | Exploiting a valid session token to impersonate a legitimate authenticated user. |
| **Session Fixation** | Forcing a victim to use a known session ID that the attacker can then hijack. |
| **MITM** | Man-in-the-Middle — an attacker positioned between two communicating parties to intercept/alter traffic. |

## References / Sources
- OWASP Session Management Cheat Sheet
- EC-Council CEH v13 Module 11

---
[⬅ Back to main README](../../README.md)
