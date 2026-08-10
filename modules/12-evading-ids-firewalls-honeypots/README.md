# Module 12 — Evading IDS, Firewalls, and Honeypots

## Overview
Detection engineering perspective on intrusion detection, honeypot deployment, and understanding firewall-evasion techniques attackers use, to build better defenses.

## Learning Objectives
- Configure and analyze IDS alerts using Snort
- Deploy the Cowrie honeypot to capture malicious interaction attempts
- Understand firewall evasion via legitimate OS utilities (BITSAdmin) — a Living-off-the-Land (LOLBin) technique

## Labs Completed
- Lab 1.1 — Detect Intrusions using Snort
- Lab 1.2 — Deploy Cowrie Honeypot
- Lab 2 — Evade Firewall through Windows BITSAdmin

## Tools & Technologies
- Snort
- Cowrie honeypot
- BITSAdmin (Windows built-in)
- pfSense/iptables

## Key Commands / Techniques
```bash
snort -A console -q -c /etc/snort/snort.conf -i eth0
docker run -p 2222:2222 cowrie/cowrie      # deploy honeypot for SSH capture
```

## Sample Payloads / Test Strings
```
N/A for this module.
```
> All commands and payloads above were executed strictly within EC-Council's isolated CEH iLabs cyber range against consenting lab targets, for educational and certification purposes only.

## Detection & Mitigation
- Tune IDS/IPS signature and anomaly rules to reduce false negatives on LOLBin abuse
- Monitor and restrict use of BITSAdmin/PowerShell/WMI via application control & logging (Sysmon)
- Deploy honeypots/honeytokens in segmented zones to generate high-fidelity alerts
- Regularly update IDS rulesets and correlate with threat intel feeds

## Key Definitions
| Term | Definition |
|---|---|
| **IDS/IPS** | Intrusion Detection/Prevention System — monitors (and optionally blocks) network traffic for malicious activity. |
| **Honeypot** | A decoy system designed to attract and log attacker activity for detection/research purposes. |
| **LOLBin** | Living-off-the-Land Binary — a legitimate OS utility abused by attackers to evade detection. |

## References / Sources
- Snort Documentation — https://www.snort.org/documents
- LOLBAS Project — https://lolbas-project.github.io
- EC-Council CEH v13 Module 12

---
[⬅ Back to main README](../../README.md)
