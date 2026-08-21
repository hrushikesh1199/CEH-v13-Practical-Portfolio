# CEH v13 Scenario-Based Question Decision Guide

A quick framework for solving difficult CEH v13 scenario-based questions.

---

## 1. First Identify the Objective

Ask:

- What is the attacker trying to achieve?
- What information is available?
- What stage of the attack is described?
- Is the question asking for a tool, technique, attack, mitigation, or next step?

```text
Reconnaissance → Information gathering
Scanning       → Hosts / ports / services
Enumeration    → Detailed service information
Vulnerability  → Weakness identification
Exploitation   → Gain unauthorized access
Post-Exploitation → Maintain / expand access
Reporting      → Document and remediate

## 2. Tool Selection

Do not choose a tool just because it is familiar.

```
Objective
    ↓
Target
    ↓
Protocol / Service
    ↓
Technique
    ↓
Appropriate Tool
```

### Examples

| Scenario | Likely Tool |
|---|---|
| Discover open ports | Nmap |
| Web proxy/testing | Burp Suite |
| SQL injection testing | sqlmap |
| Vulnerability scanning | Nessus / OpenVAS |
| Packet analysis | Wireshark |
| Password auditing | Hydra / Hashcat |
| Active Directory enumeration | PowerView / AD tools |
| Exploitation framework | Metasploit |
| Wireless assessment | Aircrack-ng |
| Cloud posture assessment | Prowler / ScoutSuite |

## 3. Identify the Protocol

If the question gives a port, map it to the service.

```
22   → SSH
23   → Telnet
25   → SMTP
53   → DNS
80   → HTTP
110  → POP3
135  → MSRPC
139  → NetBIOS
143  → IMAP
161  → SNMP
389  → LDAP
443  → HTTPS
445  → SMB
1433 → MSSQL
3306 → MySQL
3389 → RDP
5432 → PostgreSQL
5985 → WinRM
```

> **Remember:** A port suggests a service; verify the actual service during assessment.

## 4. Recognize Common Attack Patterns

### Credential Attacks
```
Many passwords → One account
    = Brute Force

One/few passwords → Many accounts
    = Password Spraying

Known leaked credentials
    = Credential Stuffing

Captured password hash
    = Offline Cracking
```

## 5. Web Vulnerability Recognition

### SQL Injection
Look for:
- User input reaching database queries
- Database errors
- Unexpected query behavior
- Unsafe dynamic SQL

```
Input
 ↓
SQL Query
 ↓
Unsafe concatenation
 ↓
Query manipulation
```

### XSS
Look for:
- User-controlled content
- Script execution in browser
- Reflected or stored input

### IDOR / BOLA
Look for:
- Object identifiers in requests
- Changing IDs
- Accessing another user's resource
- Missing server-side authorization

### SSRF
Look for:
- Server fetching a user-controlled URL
- Access to internal services
- Cloud metadata exposure

### XXE
Look for:
- XML input
- Unsafe XML parser
- External entity processing

## 6. Windows / Active Directory Recognition

### Kerberoasting
```
Service account
      ↓
SPN
      ↓
Kerberos service ticket
      ↓
Offline password cracking
```

### Pass-the-Hash
```
NTLM hash
    ↓
Authentication
    ↓
No plaintext password required
```

### Pass-the-Ticket
```
Kerberos ticket
      ↓
Reuse ticket
      ↓
Access service
```

### DCSync
```
Compromised replication privileges
        ↓
Request directory replication data
        ↓
Credential material obtained
```

## 7. Linux Privilege Escalation Recognition

Look for:
- SUID/SGID binaries
- Writable privileged files
- Weak cron jobs
- Misconfigured services
- Dangerous capabilities
- Kernel vulnerabilities
- Weak sudo configuration

```
Low Privilege User
        ↓
Enumeration
        ↓
Misconfiguration / Vulnerability
        ↓
Privilege Escalation
```

## 8. Sniffing Questions

If the scenario involves:
- Packet capture
- Network traffic
- Protocol inspection
- Credential exposure
- Suspicious packets

Think: **Wireshark** · **tcpdump** · **Snort**

## 9. Social Engineering Questions

| Scenario | Technique |
|---|---|
| Fake trusted identity | Pretexting |
| Malicious email | Phishing |
| Targeted phishing | Spear phishing |
| Executive targeted | Whaling |
| Free/tempting object | Baiting |
| Physical following | Tailgating |
| Fake exchange of service | Quid pro quo |

## 10. DoS / DDoS Recognition

```
Single source
    ↓
DoS

Multiple distributed sources
    ↓
DDoS
```

Common categories:
- Volumetric
- Protocol
- Application-layer
- Reflection/amplification

## 11. IDS / Firewall Questions

If the question asks about bypassing or evasion, look for concepts such as:
- Fragmentation
- Encoding
- Encryption
- Tunneling
- Proxying
- Obfuscation

If the question asks for defense:
```
Normalization
+
Behavioral detection
+
Correlation
+
Endpoint telemetry
```

## 12. Cloud Security Questions

Look for:
- Public storage
- Excessive IAM permissions
- Exposed credentials
- Open security groups
- Missing logging
- Container vulnerabilities

Think: IAM · Storage · Network · Secrets · Logging · Containers

## 13. "BEST" / "MOST APPROPRIATE" Questions

When several answers appear technically possible:
1. Identify the exact objective.
2. Eliminate tools that don't directly address it.
3. Prefer the answer that matches the stated scope.
4. Prefer the least invasive appropriate technique.
5. Check whether the question asks for detection, exploitation, or mitigation.

Pay attention to words such as: **BEST · FIRST · MOST EFFECTIVE · NEXT · LEAST · PRIMARY**

## 14. Attack vs Mitigation

Always distinguish these.

```
Question: "What technique could an attacker use?"
→ Attack / technique

Question: "How should the organization prevent it?"
→ Mitigation

Question: "How would a SOC detect it?"
→ Detection

Question: "What should the pentester do next?"
→ Methodology / next step
```

## Final CEH Decision Tree

```
                 SCENARIO
                    |
                    ↓
             What is the goal?
                    |
        ┌───────────┼───────────┐
        ↓           ↓           ↓
      Recon      Exploit     Defend
        |           |           |
        ↓           ↓           ↓
 Information    Technique    Mitigation
        |           |           |
        ↓           ↓           ↓
     Tool        Tool/Attack   Control
        |
        ↓
 Protocol / Port
        |
        ↓
 Validate the answer
        |
        ↓
 Check the exact wording
```

## Golden Exam Rule

Do not choose the answer that sounds the most advanced.

Choose the answer that most directly satisfies the objective described in the scenario.

---

> **Ethical Use:** All techniques and tools referenced in this repository are intended for authorized security testing, education, and controlled laboratory environments.