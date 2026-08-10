# Module 17 — Hacking Mobile Platforms

## Overview
Android platform security assessment via ADB exploitation and malicious APK concepts, alongside mobile threat-defense controls.

## Learning Objectives
- Exploit exposed Android Debug Bridge (ADB) services using PhoneSploit-Pro
- Understand malicious APK creation concepts (AndroRAT) at a conceptual/detection level
- Secure Android devices against malicious apps using AVG mobile security

## Labs Completed
- Lab 1.1 — Exploit Android via ADB Using PhoneSploit-Pro
- Lab 1.2 — Malicious APK Concepts (AndroRAT) — conceptual/detection study only
- Lab 2 — Secure Android Devices Using AVG

## Tools & Technologies
- ADB (Android Debug Bridge)
- PhoneSploit-Pro
- AVG Mobile Security
- MobSF (Mobile Security Framework)

## Key Commands / Techniques
```bash
adb connect <device-ip>:5555
adb shell   # only against devices you own with debugging intentionally enabled
adb install app-release.apk
```

## Sample Payloads / Test Strings
```
N/A for this module.
```
> All commands and payloads above were executed strictly within EC-Council's isolated CEH iLabs cyber range against consenting lab targets, for educational and certification purposes only.

## Detection & Mitigation
- Disable ADB over network (Wi-Fi debugging) on production/personal devices
- Install apps only from verified stores (Google Play Protect) and enable app scanning
- Enforce Mobile Device Management (MDM) policies for corporate-owned devices
- Keep Android OS and security patches current
- Use runtime application self-protection (RASP) for sensitive enterprise mobile apps

## Key Definitions
| Term | Definition |
|---|---|
| **ADB** | Android Debug Bridge — a developer tool providing shell access to an Android device; dangerous if exposed over the network. |
| **APK** | Android Package Kit — the installable application file format for Android. |
| **MDM** | Mobile Device Management — centralized policy enforcement and control for mobile fleets. |

## References / Sources
- Android Developers — ADB Documentation
- OWASP Mobile Application Security (MASVS)
- EC-Council CEH v13 Module 17

---
[⬅ Back to main README](../../README.md)
