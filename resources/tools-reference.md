# Tools Reference

Consolidated list of all tools used across the CEH v13 curriculum:

- AADInternals (PowerShell)
- AD Explorer
- ADB (Android Debug Bridge)
- AVG Mobile Security
- AWS CLI
- Aircrack-ng suite (airmon-ng, airodump-ng, aireplay-ng)
- Anti DDoS Guardian
- BITSAdmin (Windows built-in)
- Burp Suite
- CEH iLabs Cloud Range
- CVE/CVSS databases
- CWE
- Caido
- Cain & Abel (concept)
- Cloud-based scrubbing/WAF (concept)
- Cowrie honeypot
- CrackMapExec
- CryptoForge
- CurrPorts
- CyberChef
- DNSDumpster
- Detect It Easy (DIE)
- GoPhish (awareness campaigns)
- Google Dorks/GHDB
- Hetty
- Hybrid Analysis (sandbox)
- Hydra
- IDA Free
- Impacket (GetNPUsers/GetUserSPNs)
- Log4Shell lab range (isolated)
- Metasploit
- Metasploit Framework (auxiliary/scanner)
- Mimikatz (concept-level)
- MobSF (Mobile Security Framework)
- N-Stalker
- Nessus
- Netcraft
- Nmap
- Nmap NSE (http-*)
- Nmap NSE (smtp-enum-users)
- OWASP ZAP
- OllyDbg
- OpenSSL
- OpenVAS/GVM
- Parrot/Kali Security OS
- PhoneSploit-Pro
- PowerView
- Process Monitor (Sysinternals)
- RPCScan
- Recon-ng
- Responder
- ScoutSuite / Prowler (cloud posture)
- ShellGPT
- Sherlock
- Shodan
- SmartScanner
- Snort
- Social-Engineer Toolkit (SET)
- SuperEnum
- TCPView
- Telnet
- Trivy
- VeraCrypt
- VirusTotal
- WHOIS/Domain Tools
- Windows Event Viewer
- Windows/Linux victim VMs
- Wireshark
- Wireshark (traffic baseline analysis)
- Yersinia
- Zenmap
- arpwatch
- auditd
- can-utils (SocketCAN)
- dig
- dig (AXFR)
- eMailTrackerPro
- hping3
- macof (dsniff suite)
- nbtstat
- net view
- nslookup
- pfSense/iptables
- snmpwalk
- sqlmap
- traceroute/tracert





---

## Quick Tool Mapping

### 🔎 Footprinting & Reconnaissance

| Tool | Primary Use |
|---|---|
| WHOIS | Domain registration and ownership information |
| DNSDumpster | DNS and subdomain reconnaissance |
| Shodan | Discover internet-exposed services and devices |
| Netcraft | Website and infrastructure reconnaissance |
| Recon-ng | Automated reconnaissance framework |
| theHarvester | Collect emails, hosts and public information |
| Google Dorks | Search-engine based information discovery |
| Sherlock | Username/account enumeration |

### 🌐 Scanning & Enumeration

| Tool | Primary Use |
|---|---|
| Nmap | Host discovery, port scanning and service enumeration |
| Nmap NSE | Automated scripts for service discovery and security checks |
| Zenmap | GUI frontend for Nmap |
| SuperEnum | Automated enumeration workflow |
| RPCScan | RPC service enumeration |
| snmpwalk | SNMP enumeration |
| nbtstat | NetBIOS information gathering |
| net view | Windows network/share enumeration |
| enum4linux | SMB/Windows enumeration |

### 🔐 Vulnerability Analysis

| Tool | Primary Use |
|---|---|
| Nessus | Vulnerability assessment |
| OpenVAS/GVM | Open-source vulnerability scanning |
| N-Stalker | Web vulnerability assessment |
| Nikto | Web server security testing |
| Trivy | Container and infrastructure vulnerability scanning |
| CVE/CVSS | Vulnerability identification and severity assessment |
| CWE | Weakness classification |

### 🌐 Web Application Security

| Tool | Primary Use |
|---|---|
| Burp Suite | Web application security testing |
| OWASP ZAP | Web application vulnerability scanning and testing |
| Caido | Modern web security testing proxy |
| sqlmap | Automated SQL injection testing |
| Hetty | HTTP proxy and web security testing |
| SmartScanner | Web/application security scanning |

### 💥 Exploitation

| Tool | Primary Use |
|---|---|
| Metasploit Framework | Exploitation and post-exploitation framework |
| Hydra | Network service password auditing |
| Impacket | Windows/Active Directory protocol interaction |
| CrackMapExec | Windows/SMB/Active Directory assessment |
| Responder | LLMNR/NBT-NS/MDNS poisoning assessment |
| Mimikatz | Windows credential/security testing |
| AADInternals | Microsoft Entra ID/Azure AD security research |

### 🪟 Windows Security

| Tool | Primary Use |
|---|---|
| PowerView | Active Directory reconnaissance |
| AD Explorer | Active Directory inspection |
| Process Monitor | Windows process/file/registry monitoring |
| TCPView | Network connection monitoring |
| Windows Event Viewer | Windows security event analysis |
| BITSAdmin | Windows Background Intelligent Transfer Service interaction |

### 🐧 Linux & Network Security

| Tool | Primary Use |
|---|---|
| auditd | Linux security auditing |
| Wireshark | Packet capture and protocol analysis |
| tcpdump | Command-line packet capture |
| hping3 | Custom TCP/IP packet generation and network testing |
| arpwatch | ARP activity monitoring |
| Yersinia | Network protocol security testing |
| macof | Ethernet/MAC flooding testing |

### 📡 Wireless Security

| Tool | Primary Use |
|---|---|
| Aircrack-ng | Wireless security assessment |
| airmon-ng | Wireless monitor-mode management |
| airodump-ng | Wireless packet capture |
| aireplay-ng | Wireless frame injection/testing |
| Wireshark | Wireless traffic analysis |

### ☁️ Cloud Security

| Tool | Primary Use |
|---|---|
| AWS CLI | AWS resource administration and security assessment |
| ScoutSuite | Multi-cloud security auditing |
| Prowler | Cloud security assessment |
| Trivy | Container and cloud-native security scanning |

### 📱 Mobile Security

| Tool | Primary Use |
|---|---|
| MobSF | Mobile application security testing |
| ADB | Android device/application interaction |
| PhoneSploit-Pro | Android security testing automation |
| AVG Mobile Security | Mobile security analysis |

### 🦠 Malware & Reverse Engineering

| Tool | Primary Use |
|---|---|
| IDA Free | Reverse engineering and binary analysis |
| OllyDbg | Windows debugging |
| Detect It Easy (DIE) | File/compiler/packer identification |
| Hybrid Analysis | Malware sandbox analysis |
| VirusTotal | File, URL and indicator analysis |
| CyberChef | Encoding, decoding and data transformation |

### 🕵️ Social Engineering

| Tool | Primary Use |
|---|---|
| GoPhish | Phishing-awareness simulations |
| Social-Engineer Toolkit (SET) | Social-engineering security testing |
| eMailTrackerPro | Email header/tracing analysis |

### 📡 Sniffing & Traffic Analysis

| Tool | Primary Use |
|---|---|
| Wireshark | Graphical packet analysis |
| tcpdump | CLI packet capture |
| Snort | Network intrusion detection |
| arpwatch | ARP monitoring |
| macof | Layer-2 traffic/security testing |

### 🔒 Cryptography & File Security

| Tool | Primary Use |
|---|---|
| OpenSSL | Cryptographic operations and certificate testing |
| VeraCrypt | Encrypted volume/file protection |
| CryptoForge | File encryption |
| CyberChef | Encoding, decoding and cryptographic transformations |

---

## 🧠 CEH Exam Memory Map

```text
RECON
  ↓
WHOIS → DNSDumpster → Shodan → Recon-ng

SCANNING
  ↓
Nmap → NSE → Zenmap → SuperEnum

ENUMERATION
  ↓
SMB → RPC → SNMP → NetBIOS

VULNERABILITY ANALYSIS
  ↓
Nessus → OpenVAS → N-Stalker → CVE/CVSS

WEB SECURITY
  ↓
Burp Suite → ZAP → sqlmap → Caido

EXPLOITATION
  ↓
Metasploit → Hydra → Impacket → CrackMapExec

SNIFFING
  ↓
Wireshark → tcpdump → Snort

WIRELESS
  ↓
Aircrack-ng → airodump-ng → aireplay-ng

SOCIAL ENGINEERING
  ↓
SET → GoPhish

MALWARE
  ↓
IDA → DIE → Hybrid Analysis → VirusTotal

CLOUD
  ↓
AWS CLI → ScoutSuite → Prowler → Trivy