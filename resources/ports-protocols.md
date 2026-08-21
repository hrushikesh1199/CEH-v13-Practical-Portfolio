# CEH v13 Ports & Protocols Quick Reference

Quick revision reference for commonly tested network services, ports, protocols, and security concepts.

---

## 🌐 Common Network Services

| Port | Protocol / Service | Transport | Common Purpose |
|---:|---|---|---|
| 20 | FTP-Data | TCP | FTP data transfer |
| 21 | FTP | TCP | File Transfer Protocol |
| 22 | SSH | TCP | Secure remote administration |
| 23 | Telnet | TCP | Remote administration |
| 25 | SMTP | TCP | Email transmission |
| 53 | DNS | TCP/UDP | Domain name resolution |
| 67/68 | DHCP | UDP | Dynamic IP assignment |
| 69 | TFTP | UDP | Trivial File Transfer |
| 80 | HTTP | TCP | Web traffic |
| 110 | POP3 | TCP | Email retrieval |
| 111 | RPCbind | TCP/UDP | RPC service mapping |
| 123 | NTP | UDP | Time synchronization |
| 135 | MSRPC | TCP | Microsoft RPC |
| 137 | NetBIOS-NS | UDP | Name service |
| 138 | NetBIOS-DGM | UDP | Datagram service |
| 139 | NetBIOS-SSN | TCP | Session service |
| 143 | IMAP | TCP | Email retrieval |
| 161 | SNMP | UDP | Network management |
| 162 | SNMP Trap | UDP | SNMP notifications |
| 389 | LDAP | TCP/UDP | Directory services |
| 443 | HTTPS | TCP | Secure web traffic |
| 445 | SMB | TCP | Windows file/printer sharing |
| 465 | SMTPS | TCP | SMTP over TLS |
| 514 | Syslog | UDP/TCP | Logging |
| 587 | SMTP Submission | TCP | Email submission |
| 636 | LDAPS | TCP | LDAP over TLS |
| 993 | IMAPS | TCP | IMAP over TLS |
| 995 | POP3S | TCP | POP3 over TLS |
| 1433 | MS SQL Server | TCP | Microsoft SQL Server |
| 1521 | Oracle DB | TCP | Oracle database |
| 2049 | NFS | TCP/UDP | Network File System |
| 3306 | MySQL | TCP | MySQL database |
| 3389 | RDP | TCP/UDP | Windows Remote Desktop |
| 5432 | PostgreSQL | TCP | PostgreSQL database |
| 5900 | VNC | TCP | Remote desktop |
| 5985 | WinRM HTTP | TCP | Windows Remote Management |
| 5986 | WinRM HTTPS | TCP | Secure Windows Remote Management |
| 6379 | Redis | TCP | In-memory database |
| 8080 | HTTP Alternate | TCP | Alternate web service |

---

## 🔎 Enumeration Mapping

| Service | Port | Useful Enumeration Focus |
|---|---:|---|
| FTP | 21 | Anonymous access, banner, commands |
| SSH | 22 | Version, authentication methods |
| SMTP | 25 | Server information, user enumeration |
| DNS | 53 | Records, zone transfer, subdomains |
| HTTP | 80 | Web technologies, directories, headers |
| RPC | 111 | RPC services and exposed procedures |
| NetBIOS | 137-139 | Hostnames, shares, sessions |
| SNMP | 161 | Community strings and system information |
| LDAP | 389 | Directory information |
| SMB | 445 | Shares, users, domain information |
| RDP | 3389 | Remote desktop exposure |
| WinRM | 5985/5986 | Remote management |

---

## 🛡️ Security Protocols

| Protocol | Security Purpose |
|---|---|
| SSH | Encrypted remote administration |
| HTTPS | Encrypted HTTP communication |
| TLS | Transport-layer encryption |
| IPsec | Network-layer security |
| SFTP | Secure file transfer over SSH |
| LDAPS | LDAP over TLS |
| SNMPv3 | Authenticated and encrypted SNMP |
| Kerberos | Network authentication |
| WPA2/WPA3 | Wireless security |

---

## ⚠️ Common Insecure Protocols

| Protocol | Risk |
|---|---|
| Telnet | Credentials/data transmitted without encryption |
| FTP | Authentication/data can be exposed |
| HTTP | Traffic is not encrypted |
| TFTP | Minimal authentication/security |
| SNMPv1/v2c | Community strings may be exposed |
| POP3 | Unencrypted email retrieval without TLS |
| IMAP | Unencrypted email retrieval without TLS |

---

## 🧠 CEH Port Memory Groups

### Remote Access

```text
22    SSH
23    Telnet
3389  RDP
5900  VNC
5985  WinRM
5986  WinRM HTTPS



## Common Ports & Services

### Web
```
80    HTTP
443   HTTPS
8080  HTTP Alternate
```

### Email
```
25    SMTP
110   POP3
143   IMAP
465   SMTPS
587   SMTP Submission
993   IMAPS
995   POP3S
```

### Windows / Active Directory
```
135   MSRPC
137   NetBIOS-NS
138   NetBIOS-DGM
139   NetBIOS-SSN
389   LDAP
445   SMB
636   LDAPS
3389  RDP
5985  WinRM
5986  WinRM HTTPS
```

### Databases
```
1433  MS SQL
1521  Oracle
3306  MySQL
5432  PostgreSQL
6379  Redis
```

### Network Management
```
53     DNS
67/68  DHCP
111    RPCbind
123    NTP
161    SNMP
162    SNMP Trap
514    Syslog
```

## 🔥 Scenario-Based Exam Thinking

When a CEH question gives you a port, first identify the service.

```
Port
  ↓
Service
  ↓
Protocol
  ↓
Typical Function
  ↓
Potential Security Weakness
  ↓
Appropriate Assessment Tool
```

### Example
```
445
  ↓
SMB
  ↓
Windows file/printer sharing
  ↓
Enumerate shares/users/domain information
  ↓
Check for weak configuration or exposed resources
  ↓
Use appropriate SMB enumeration tools
```

## 📌 Quick Exam Rules

- TCP and UDP are different transport protocols.
- TCP provides connection-oriented communication.
- UDP is connectionless.
- DNS commonly uses UDP 53, but TCP 53 is also used in specific situations.
- HTTPS commonly uses TCP 443.
- SMB commonly uses TCP 445.
- SSH commonly uses TCP 22.
- RDP commonly uses TCP/UDP 3389.
- SNMP commonly uses UDP 161.
- SNMP traps commonly use UDP 162.
- LDAP commonly uses TCP/UDP 389.
- LDAPS commonly uses TCP 636.

> Ports and services can be changed or configured on non-standard ports. Never assume that a port alone proves what service is running; verify the service during authorized assessment.