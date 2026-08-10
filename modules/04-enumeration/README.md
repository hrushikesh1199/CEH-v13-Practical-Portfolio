# Module 04 — Enumeration

## Overview
Extraction of detailed system, user, and network information from identified services (NetBIOS, SNMP, LDAP, NFS, DNS, SMTP) to build actionable attack vectors.

## Learning Objectives
- Enumerate NetBIOS shares, sessions, and user accounts
- Perform SNMP enumeration using community strings
- Enumerate Active Directory objects via LDAP
- Enumerate NFS exports and shares
- Perform DNS zone transfer enumeration
- Enumerate SMTP users via VRFY/EXPN

## Labs Completed
- Lab 1 — NetBIOS Enumeration using Windows Command-Line Utilities
- Lab 2 — SNMP Enumeration using SnmpWalk
- Lab 3 — LDAP Enumeration using AD Explorer
- Lab 4 — NFS Enumeration using RPCScan and SuperEnum
- Lab 5 — DNS Enumeration using Zone Transfer
- Lab 6 — SMTP Enumeration using Nmap
- Lab 7 — Enumeration using Global Network Inventory
- Lab 8 — Enumeration using ShellGPT

## Tools & Technologies
- nbtstat
- net view
- snmpwalk
- AD Explorer
- RPCScan
- SuperEnum
- dig (AXFR)
- Nmap NSE (smtp-enum-users)

## Key Commands / Techniques
```bash
nbtstat -A 192.168.1.10
net view \\target
snmpwalk -v2c -c public target.com
showmount -e target.com
dig axfr @ns1.target.com target.com
nmap -p25 --script smtp-enum-users target.com
```

## Sample Payloads / Test Strings
```
N/A for this module.
```
> All commands and payloads above were executed strictly within EC-Council's isolated CEH iLabs cyber range against consenting lab targets, for educational and certification purposes only.

## Detection & Mitigation
- Disable NetBIOS/SMBv1 where not required; enforce SMB signing
- Change default SNMP community strings ('public'/'private') and migrate to SNMPv3
- Restrict zone transfers (AXFR) to authorized secondary DNS servers only
- Disable SMTP VRFY/EXPN commands or restrict to authenticated relays
- Apply least-privilege on NFS exports with host-based access control

## Key Definitions
| Term | Definition |
|---|---|
| **Enumeration** | The process of actively extracting usernames, machine names, shares, and services from a system after initial scanning. |
| **Zone Transfer (AXFR)** | A DNS mechanism to replicate zone data between servers; misconfiguration can leak entire DNS records to attackers. |
| **SNMP Community String** | A password-like value used to authenticate to SNMP-managed devices. |

## References / Sources
- EC-Council CEH v13 Module 04
- CIS Benchmarks — https://www.cisecurity.org/cis-benchmarks

---
[⬅ Back to main README](../../README.md)
