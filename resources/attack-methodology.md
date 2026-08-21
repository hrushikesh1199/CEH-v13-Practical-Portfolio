# CEH v13 Attack Methodology Quick Reference

A practical revision map for connecting CEH techniques, objectives, tools, and defensive considerations.

---

## 1. Reconnaissance

**Goal:** Collect information about the target before active testing.

### Passive Recon
- WHOIS
- DNS records
- Search engines / Google Dorks
- Shodan
- Netcraft
- Social media / public profiles
- Certificate transparency

### Active Recon
- DNS enumeration
- Host discovery
- Service discovery
- Network scanning

### Common Tools
`WHOIS` `DNSDumpster` `theHarvester` `Recon-ng` `Shodan` `Nmap`

---

## 2. Scanning

**Goal:** Identify live hosts, open ports, services, and potential weaknesses.

### Typical Flow

```text
Host Discovery
     ↓
Port Scanning
     ↓
Service Detection
     ↓
OS Detection
     ↓
NSE / Vulnerability Checks


## Common Tools
- Nmap
- Zenmap
- Nmap NSE
- Nessus
- OpenVAS/GVM

### Important Nmap Concepts
```
-sS     SYN scan
-sT     TCP connect scan
-sU     UDP scan
-sV     Service/version detection
-O      OS detection
-A      Aggressive detection
-p      Port selection
-sn     Host discovery
```

## 3. Enumeration
**Goal:** Extract detailed information from discovered services.

### Common Targets
- SMB
- FTP
- SMTP
- SNMP
- DNS
- LDAP
- RPC
- NetBIOS

### Common Tools
`snmpwalk` · `nbtstat` · `net view` · RPCScan · Nmap NSE

## 4. Vulnerability Analysis
**Goal:** Identify and prioritize security weaknesses.

### Important Concepts
- **CVE** → Vulnerability identifier
- **CWE** → Weakness classification
- **CVSS** → Severity scoring

### Common Tools
Nessus · OpenVAS/GVM · Nmap NSE · N-Stalker · Trivy

## 5. System Hacking
**Goal:** Assess authentication, credentials, access controls, and system security.

### Credential Attack Categories
- Brute Force
- Dictionary Attack
- Password Spraying
- Credential Stuffing
- Rainbow Table
- Offline Cracking

### Common Tools
Hydra · Hashcat · Mimikatz

## 6. Malware Threats

### Analysis Workflow
```
Sample
  ↓
Hash
  ↓
Static Analysis
  ↓
Dynamic Analysis
  ↓
Behavior Analysis
  ↓
Indicators of Compromise
```

### Common Tools
VirusTotal · Hybrid Analysis · IDA Free · Detect It Easy · OllyDbg

## 7. Sniffing
**Goal:** Capture and analyze network traffic.

### Common Tools
- Wireshark
- tcpdump
- Snort
- arpwatch

### Key Concepts
```
Packet Capture
      ↓
Protocol Analysis
      ↓
Credential / Data Exposure
      ↓
Detection & Mitigation
```

## 8. Social Engineering
**Goal:** Test whether humans can be manipulated into violating security controls.

### Common Techniques
- Phishing
- Spear phishing
- Whaling
- Pretexting
- Baiting
- Tailgating
- Quid pro quo

### Common Tools
GoPhish · SET

> **Important:** Perform social-engineering simulations only with explicit authorization.

## 9. Denial of Service

### Major Categories
- Volumetric
- Protocol
- Application Layer
- Distributed DoS

### Common Concepts
- SYN flood
- UDP flood
- HTTP flood
- Resource exhaustion
- Reflection/amplification

### Defensive Controls
- Rate limiting
- Traffic filtering
- WAF
- CDN
- DDoS protection
- Load balancing

## 10. Session Hijacking
**Goal:** Obtain or abuse an authenticated session.

### Important Concepts
- Session cookies
- Session IDs
- Session fixation
- Session theft
- Cookie security

### Defensive Controls
- Secure
- HttpOnly
- SameSite
- Session rotation and expiration

## 11. Evading IDS / Firewalls

### Concepts
- Traffic fragmentation
- Encoding
- Tunneling
- Proxying
- Encryption
- Traffic obfuscation

### Defensive Perspective
Detection systems should use:
- Network normalization
- Behavioral detection
- Correlation
- Multiple telemetry sources
- Endpoint visibility

## 12. Web Server Hacking

### Assessment Areas
```
Server Fingerprinting
        ↓
Directory Discovery
        ↓
Configuration Review
        ↓
Known Vulnerabilities
        ↓
Authentication
        ↓
Access Control
```

### Common Tools
Nmap · Nikto · Burp Suite · OWASP ZAP

## 13. Web Application Security

### Core Testing Areas
- Authentication
- Authorization
- Session management
- Input validation
- Injection
- File upload
- SSRF
- XXE
- XSS
- CSRF
- Security misconfiguration

### Common Tools
Burp Suite · OWASP ZAP · Caido · sqlmap

## 14. SQL Injection

### Concept
```
Application Input
       ↓
SQL Query
       ↓
Unsafe Input Handling
       ↓
Query Manipulation
```

### Testing Focus
- Error-based behavior
- Boolean-based behavior
- Time-based behavior
- Union-based behavior

### Tool
sqlmap

> Always test only authorized applications.

## 15. Cloud Security

### Assessment Areas
- IAM
- Storage permissions
- Network exposure
- Security groups
- Logging
- Secrets
- Misconfiguration
- Container security

### Common Tools
AWS CLI · ScoutSuite · Prowler · Trivy

## 16. Wireless Security

### Assessment Flow
```
Identify Network
      ↓
Capture Traffic
      ↓
Analyze Authentication
      ↓
Assess Configuration
      ↓
Report Findings
```

### Common Tools
Aircrack-ng · airodump-ng · aireplay-ng · Wireshark

## CEH Exam Thinking Framework

For scenario-based questions, think:

```
What is the objective?
        ↓
What information is available?
        ↓
Which technique matches the objective?
        ↓
Which tool supports that technique?
        ↓
Which protocol / port is involved?
        ↓
What is the most appropriate next step?
        ↓
What mitigation would prevent it?
```

## Pentesting Lifecycle
```
1. Planning
      ↓
2. Reconnaissance
      ↓
3. Scanning
      ↓
4. Enumeration
      ↓
5. Vulnerability Analysis
      ↓
6. Exploitation
      ↓
7. Post-Exploitation
      ↓
8. Reporting
      ↓
9. Remediation / Retesting
```

## Defensive Mindset

A good ethical hacker should be able to answer three questions:
1. How could this weakness be identified?
2. What security impact could it create?
3. How can the organization detect and prevent it?

---

> All techniques in this repository are intended for authorized security testing, education, and controlled laboratory environments.