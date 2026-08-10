# Module 02 — Footprinting and Reconnaissance

## Overview
Passive and active information gathering techniques used to build a profile of a target organization prior to active engagement, including OSINT, DNS enumeration, and social-media-based reconnaissance.

## Learning Objectives
- Perform advanced Google Dorking / Google Hacking Database (GHDB) queries
- Enumerate subdomains and hosting infrastructure using Netcraft and DNSDumpster
- Conduct OSINT against individuals using Sherlock across social platforms
- Perform WHOIS lookups to identify domain registration data
- Query authoritative DNS records using nslookup / dig
- Trace network paths using traceroute/tracert
- Trace email headers/origin using eMailTrackerPro
- Automate footprinting using Recon-ng and AI-assisted tooling (ShellGPT)

## Labs Completed
- Lab 1 — Gather Hacking Information Using Advanced Google Hacking Techniques
- Lab 2 — Find Domains, Sub-domains and Hosts using Netcraft and DNSDumpster
- Lab 3 — Gather Personal Information from Social Networking Sites Using Sherlock
- Lab 4 — Perform WHOIS Lookup using Domain Tools
- Lab 5 — Gather DNS Information using nslookup and Online Tools
- Lab 6 — Perform Network Tracerouting (Windows & Linux)
- Lab 7 — Trace a Target via Email Headers using eMailTrackerPro
- Lab 8 — Footprinting a Target using Recon-ng
- Lab 9 — Footprinting a Target using ShellGPT

## Tools & Technologies
- Google Dorks/GHDB
- Netcraft
- DNSDumpster
- Sherlock
- WHOIS/Domain Tools
- nslookup
- dig
- traceroute/tracert
- eMailTrackerPro
- Recon-ng
- ShellGPT

## Key Commands / Techniques
```bash
nslookup -type=ANY target.com
dig target.com ANY +noall +answer
whois target.com
traceroute target.com          # Linux
tracert target.com             # Windows
python3 sherlock.py target_username
recon-ng -> workspaces create target -> marketplace install recon/domains-hosts/hackertarget
```

## Sample Payloads / Test Strings
```
site:target.com filetype:pdf
site:target.com inurl:admin
intitle:"index of" target.com
```
> All commands and payloads above were executed strictly within EC-Council's isolated CEH iLabs cyber range against consenting lab targets, for educational and certification purposes only.

## Detection & Mitigation
- Minimize publicly exposed metadata (document authors, server banners, employee emails)
- Enforce WHOIS privacy/registrar-lock on organizational domains
- Monitor and restrict subdomain sprawl; deprecate/deregister unused DNS records
- Conduct periodic OSINT self-assessments (attack surface management)
- Employee awareness training on social media exposure and phishing indicators

## Key Definitions
| Term | Definition |
|---|---|
| **OSINT** | Open Source Intelligence — information collected from publicly available sources. |
| **Footprinting** | The process of accumulating data about a specific target environment, usually the first step of an attack lifecycle. |
| **Passive Reconnaissance** | Gathering information without directly interacting with the target's systems (e.g., WHOIS, search engines). |
| **Active Reconnaissance** | Gathering information via direct interaction with target systems (e.g., traceroute, DNS queries). |

## References / Sources
- OWASP Testing Guide — Information Gathering
- Google Hacking Database (GHDB) — https://www.exploit-db.com/google-hacking-database
- EC-Council CEH v13 Module 02

---
[⬅ Back to main README](../../README.md)
