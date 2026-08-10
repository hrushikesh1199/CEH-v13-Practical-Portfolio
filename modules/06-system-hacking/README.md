# Module 06 — System Hacking

## Overview
End-to-end exploitation lifecycle: credential attacks, privilege escalation, persistence, and anti-forensic log clearing, including a full Active Directory attack chain (AS-REP Roasting, Kerberoasting, privilege escalation).

## Learning Objectives
- Perform password cracking/relay attacks using Responder
- Establish remote access via reverse shells
- Understand buffer overflow exploitation fundamentals
- Bypass UAC and abuse Sticky Keys for privilege escalation
- Understand monitoring/surveillance tooling and detection evasion
- Establish persistence via registry Run keys
- Clear Windows and Linux logs (anti-forensics awareness)
- Execute an AD attack chain: recon → AS-REP Roasting → password spraying → Kerberoasting → privilege escalation

## Labs Completed
- Lab 1.1 — Active Online Attack / Password Cracking using Responder
- Lab 1.2 — Gain Remote Access using Reverse Shell Generator
- Lab 1.3 — Buffer Overflow Attack Fundamentals
- Lab 2.1 — Escalate Privileges (UAC Bypass / Sticky Keys)
- Lab 3.1 — Monitoring & Surveillance using Spyrix
- Lab 3.2 — Persistence via Registry Run Keys
- Lab 4.1 — Clear Windows Machine Logs
- Lab 4.2 — Clear Linux Machine Logs (BASH)
- Lab 5.1-5.7 — Domain Controller Recon → AS-REP Roasting → CrackMapExec Spray → PowerView Enum → MSSQL Attack → Privilege Escalation → Kerberoasting
- Lab 6 — System Hacking using ShellGPT

## Tools & Technologies
- Responder
- Metasploit
- Mimikatz (concept-level)
- CrackMapExec
- PowerView
- Impacket (GetNPUsers/GetUserSPNs)
- Windows Event Viewer
- auditd

## Key Commands / Techniques
```bash
responder -I eth0 -wrf                                   # LLMNR/NBT-NS poisoning capture
GetNPUsers.py domain.local/ -usersfile users.txt -no-pass  # AS-REP Roasting
crackmapexec smb targets.txt -u users.txt -p passwords.txt --continue-on-success
GetUserSPNs.py domain.local/user:pass -request           # Kerberoasting
wevtutil cl System                                       # clear Windows System log (detection example only)
```

## Sample Payloads / Test Strings
```
N/A for this module.
```
> All commands and payloads above were executed strictly within EC-Council's isolated CEH iLabs cyber range against consenting lab targets, for educational and certification purposes only.

## Detection & Mitigation
- Disable LLMNR/NBT-NS to prevent Responder-style credential capture
- Enforce strong Kerberos policies: AES encryption, disable RC4, enable AES-only SPNs
- Use Managed Service Accounts / gMSA with long random passwords to defeat Kerberoasting
- Enable and centrally forward audit logs (Windows Event Forwarding / SIEM) — log clearing generates its own detectable event (ID 1102/104)
- Apply least privilege, disable local admin sharing, and require MFA for privileged access
- Enable Credential Guard and disable Sticky Keys backdoor persistence vectors

## Key Definitions
| Term | Definition |
|---|---|
| **AS-REP Roasting** | An attack against Kerberos accounts with pre-authentication disabled, allowing offline password cracking of a captured ticket. |
| **Kerberoasting** | Requesting service tickets (TGS) for SPNs and cracking them offline to recover service account passwords. |
| **Privilege Escalation** | Techniques used to gain higher-level permissions than originally granted. |
| **Persistence** | Techniques ensuring continued access to a compromised system across reboots/credential changes. |

## References / Sources
- MITRE ATT&CK — Credential Access (TA0006)
- Impacket Project — https://github.com/fortra/impacket
- EC-Council CEH v13 Module 06

---
[⬅ Back to main README](../../README.md)
