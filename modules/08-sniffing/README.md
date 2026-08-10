# Module 08 — Sniffing

## Overview
Layer-2 traffic interception techniques including MAC flooding, DHCP starvation, and passive credential capture, with corresponding detection methods.

## Learning Objectives
- Understand switch CAM table exhaustion via MAC flooding
- Understand DHCP starvation attacks using Yersinia
- Capture and analyze cleartext credentials using Wireshark
- Detect ARP poisoning and promiscuous-mode NICs on a switched network

## Labs Completed
- Lab 1.1 — MAC Flooding using macof
- Lab 1.2 — DHCP Starvation Attack using Yersinia
- Lab 2 — Password Sniffing using Wireshark
- Lab 3 — Detect ARP Poisoning and Promiscuous Mode

## Tools & Technologies
- macof (dsniff suite)
- Yersinia
- Wireshark
- arpwatch
- Cain & Abel (concept)

## Key Commands / Techniques
```bash
macof -i eth0                            # MAC flooding demo (lab-isolated network only)
wireshark -i eth0 -k -f 'tcp port 21 or tcp port 23'   # capture cleartext FTP/Telnet creds
arp -a                                    # inspect local ARP cache for anomalies
```

## Sample Payloads / Test Strings
```
N/A for this module.
```
> All commands and payloads above were executed strictly within EC-Council's isolated CEH iLabs cyber range against consenting lab targets, for educational and certification purposes only.

## Detection & Mitigation
- Enable port security (limit MAC addresses per switch port) to prevent MAC flooding
- Enable DHCP snooping to prevent starvation and rogue DHCP servers
- Enable Dynamic ARP Inspection (DAI) to prevent ARP poisoning
- Enforce encrypted protocols (SSH, HTTPS, SFTP) instead of cleartext (Telnet, FTP, HTTP)
- Deploy 802.1X port-based network access control

## Key Definitions
| Term | Definition |
|---|---|
| **MAC Flooding** | Overloading a switch's CAM table with fake MAC addresses, forcing it into hub-like broadcast mode. |
| **ARP Poisoning** | Sending forged ARP replies to associate an attacker's MAC with a victim's IP, enabling MITM. |
| **Promiscuous Mode** | A NIC mode that captures all traffic on a segment, not just traffic addressed to it. |

## References / Sources
- EC-Council CEH v13 Module 08
- Wireshark User Guide — https://www.wireshark.org/docs/

---
[⬅ Back to main README](../../README.md)
