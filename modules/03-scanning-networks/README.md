# Module 03 — Scanning Networks

## Overview
Active discovery of live hosts, open ports, running services, and operating systems to identify potential entry points, including IDS/firewall evasion techniques.

## Learning Objectives
- Perform host discovery using ICMP, ARP, and TCP/UDP probing
- Enumerate open ports and services with Nmap scan types (SYN, Connect, UDP, etc.)
- Perform OS fingerprinting using the Nmap Scripting Engine (NSE)
- Understand and apply firewall/IDS evasion techniques (fragmentation, decoys, source-port spoofing)
- Use Metasploit auxiliary modules for network scanning

## Labs Completed
- Lab 1 — Perform Host Discovery Using Nmap
- Lab 2 — Explore Network Scanning Techniques Using Nmap
- Lab 3 — Perform OS Discovery Using NSE
- Lab 4 — Scan Beyond IDS/Firewall Using Evasion Techniques
- Lab 5 — Scan a Target Network Using Metasploit
- Lab 6 — Scan a Target Using ShellGPT

## Tools & Technologies
- Nmap
- Zenmap
- Metasploit Framework (auxiliary/scanner)
- hping3

## Key Commands / Techniques
```bash
nmap -sn 192.168.1.0/24                     # host discovery
nmap -sS -p- -T4 target.com                 # full TCP SYN port scan
nmap -sU -p 53,161,500 target.com           # UDP scan
nmap -O -sV target.com                      # OS & service version detection
nmap --script vuln target.com                # NSE vulnerability scripts
nmap -f -D RND:10 target.com                 # fragmentation + decoys (evasion)
msfconsole -q -x 'use auxiliary/scanner/portscan/tcp; set RHOSTS target.com; run'
```

## Sample Payloads / Test Strings
```
N/A for this module.
```
> All commands and payloads above were executed strictly within EC-Council's isolated CEH iLabs cyber range against consenting lab targets, for educational and certification purposes only.

## Detection & Mitigation
- Deploy stateful firewalls and IDS/IPS with anomaly-based detection for scan patterns
- Disable unused/unnecessary services and close unneeded ports
- Rate-limit and alert on high-volume connection attempts from a single source
- Use network segmentation to limit lateral scanning between zones

## Key Definitions
| Term | Definition |
|---|---|
| **Port Scanning** | The technique of probing a host for open TCP/UDP ports to identify running services. |
| **OS Fingerprinting** | Identifying the target's operating system based on TCP/IP stack behavior. |
| **IDS Evasion** | Techniques (fragmentation, decoys, timing) used to avoid detection by intrusion detection systems during scanning. |

## References / Sources
- Nmap Official Reference Guide — https://nmap.org/book/
- EC-Council CEH v13 Module 03

---
[⬅ Back to main README](../../README.md)
