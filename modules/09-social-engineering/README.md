# Module 09 — Social Engineering

## Overview
Human-factor attack vectors including credential phishing pages, phishing detection, and AI-assisted phishing email crafting for awareness-training purposes.

## Learning Objectives
- Understand credential harvesting via the Social-Engineer Toolkit (SET)
- Detect phishing domains and infrastructure using Netcraft
- Understand AI-assisted phishing email generation for red-team/awareness simulation

## Labs Completed
- Lab 1 — Credential Sniffing using Social-Engineer Toolkit (SET)
- Lab 2 — Detect Phishing Using Netcraft
- Lab 3 — Craft Phishing Emails Using ChatGPT (awareness simulation)

## Tools & Technologies
- Social-Engineer Toolkit (SET)
- Netcraft
- GoPhish (awareness campaigns)

## Key Commands / Techniques
```bash
setoolkit   # menu-driven; used only in isolated lab range against consenting test targets
```

## Sample Payloads / Test Strings
```
N/A for this module.
```
> All commands and payloads above were executed strictly within EC-Council's isolated CEH iLabs cyber range against consenting lab targets, for educational and certification purposes only.

## Detection & Mitigation
- Run regular, consented phishing-simulation awareness campaigns with metrics tracking
- Deploy email security gateways with DMARC/DKIM/SPF enforcement
- Implement browser isolation / URL rewriting for inbound links
- Mandate MFA to reduce impact of credential harvesting
- Train staff to verify requests via out-of-band channels before acting

## Key Definitions
| Term | Definition |
|---|---|
| **Social Engineering** | Psychological manipulation of people into performing actions or divulging confidential information. |
| **Phishing** | Fraudulent communication, typically email, designed to trick a victim into revealing sensitive data or executing malware. |
| **Pretexting** | Creating a fabricated scenario to engage a target and extract information. |

## References / Sources
- EC-Council CEH v13 Module 09
- APWG Phishing Trends Reports — https://apwg.org

---
[⬅ Back to main README](../../README.md)
