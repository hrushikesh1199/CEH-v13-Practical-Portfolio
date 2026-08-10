# Module 10 — Denial-of-Service

## Overview
Availability attack concepts (volumetric and botnet-based DoS/DDoS) studied in a fully isolated lab range, alongside detection and mitigation tooling.

## Learning Objectives
- Understand volumetric DDoS mechanics using controlled lab tools (isolated range only)
- Understand botnet-based DDoS architecture at a conceptual level
- Deploy and configure anti-DDoS detection/mitigation tooling

## Labs Completed
- Lab 1.1 — DDoS Attack using ISB/UltraDDOS-v2 (isolated lab range only)
- Lab 1.2 — DDoS Attack Concepts using Botnets (isolated lab range only)
- Lab 2 — Detect and Protect Against DDoS using Anti DDoS Guardian

## Tools & Technologies
- Anti DDoS Guardian
- Cloud-based scrubbing/WAF (concept)
- Wireshark (traffic baseline analysis)

## Key Commands / Techniques
```bash
# Detection-side example: baseline connection-rate monitoring
netstat -an | grep :80 | wc -l
```

## Sample Payloads / Test Strings
```
N/A for this module.
```
> All commands and payloads above were executed strictly within EC-Council's isolated CEH iLabs cyber range against consenting lab targets, for educational and certification purposes only.

## Detection & Mitigation
- Deploy cloud-based DDoS scrubbing / CDN (e.g., WAF + rate limiting) in front of public services
- Implement SYN cookies and connection-rate limiting at the perimeter
- Use anycast routing and horizontal scaling to absorb volumetric load
- Maintain an incident response runbook specifically for availability attacks

## Key Definitions
| Term | Definition |
|---|---|
| **DoS** | Denial-of-Service — an attack intended to make a system or service unavailable to legitimate users. |
| **DDoS** | Distributed Denial-of-Service — a DoS attack launched from multiple distributed sources, often a botnet. |
| **Botnet** | A network of compromised devices controlled by an attacker to conduct coordinated attacks. |

## References / Sources
- EC-Council CEH v13 Module 10
- CISA DDoS Quick Reference Guide

---
[⬅ Back to main README](../../README.md)
