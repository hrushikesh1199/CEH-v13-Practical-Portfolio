# Module 18 — IoT and OT Hacking

## Overview
Reconnaissance and traffic analysis of IoT devices and industrial/operational technology protocols, including CAN bus replay attacks relevant to automotive/industrial systems.

## Learning Objectives
- Gather IoT device intelligence using online footprinting tools (e.g., Shodan)
- Capture and analyze IoT network traffic using Wireshark
- Understand CAN bus replay attack concepts in OT/automotive environments

## Labs Completed
- Lab 1 — Gather Information using Online Footprinting Tools (Shodan)
- Lab 2 — Capture and Analyze IoT Traffic using Wireshark
- Lab 3 — Perform Replay Attack on CAN Protocol

## Tools & Technologies
- Shodan
- Wireshark
- can-utils (SocketCAN)

## Key Commands / Techniques
```bash
shodan search 'default password' country:IN
candump can0                       # capture CAN bus traffic (lab/bench ECU only)
cansend can0 123#DEADBEEF          # replay a captured CAN frame (lab/bench ECU only)
```

## Sample Payloads / Test Strings
```
N/A for this module.
```
> All commands and payloads above were executed strictly within EC-Council's isolated CEH iLabs cyber range against consenting lab targets, for educational and certification purposes only.

## Detection & Mitigation
- Change default credentials on all IoT/OT devices before deployment
- Segment OT/ICS networks from IT networks (Purdue Model zoning)
- Implement CAN bus message authentication where hardware supports it
- Disable unnecessary exposed services and close internet-facing management ports
- Apply firmware update programs and vulnerability tracking specific to IoT/OT vendors

## Key Definitions
| Term | Definition |
|---|---|
| **IoT** | Internet of Things — network-connected physical devices with embedded sensors/computing. |
| **OT** | Operational Technology — hardware/software controlling physical industrial processes (ICS/SCADA). |
| **CAN Bus** | Controller Area Network — a robust vehicle/industrial bus protocol lacking native authentication, vulnerable to replay attacks. |

## References / Sources
- OWASP IoT Top 10
- CISA ICS Advisories — https://www.cisa.gov/ics
- EC-Council CEH v13 Module 18

---
[⬅ Back to main README](../../README.md)
