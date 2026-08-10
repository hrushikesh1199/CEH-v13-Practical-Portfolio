# Glossary — Ethical Hacking & Cybersecurity Terms

| Term | Definition |
|---|---|
| **4-Way Handshake** | The WPA/WPA2 authentication exchange between client and AP used to derive session keys — capturable and crackable offline if the PSK is weak. |
| **ADB** | Android Debug Bridge — a developer tool providing shell access to an Android device; dangerous if exposed over the network. |
| **APK** | Android Package Kit — the installable application file format for Android. |
| **ARP Poisoning** | Sending forged ARP replies to associate an attacker's MAC with a victim's IP, enabling MITM. |
| **AS-REP Roasting** | An attack against Kerberos accounts with pre-authentication disabled, allowing offline password cracking of a captured ticket. |
| **Active Reconnaissance** | Gathering information via direct interaction with target systems (e.g., traceroute, DNS queries). |
| **Banner Grabbing** | Extracting service/version information from a server's response headers/banners. |
| **Blind SQLi** | An injection technique where the application does not directly return query results, requiring boolean/time-based inference. |
| **Botnet** | A network of compromised devices controlled by an attacker to conduct coordinated attacks. |
| **CAN Bus** | Controller Area Network — a robust vehicle/industrial bus protocol lacking native authentication, vulnerable to replay attacks. |
| **CIA Triad** | Confidentiality, Integrity, Availability — the three core objectives of information security. |
| **CVE** | Common Vulnerabilities and Exposures — a standardized identifier for publicly known vulnerabilities. |
| **CVSS** | Common Vulnerability Scoring System — a numeric score (0-10) representing vulnerability severity. |
| **CWE** | Common Weakness Enumeration — a category system for software/hardware weakness types. |
| **DDoS** | Distributed Denial-of-Service — a DoS attack launched from multiple distributed sources, often a botnet. |
| **Deauthentication Attack** | Forcibly disconnecting a wireless client to capture a fresh handshake or perform a DoS. |
| **Directory Listing** | A web server misconfiguration exposing full directory contents to unauthenticated users. |
| **DoS** | Denial-of-Service — an attack intended to make a system or service unavailable to legitimate users. |
| **Dynamic Analysis** | Executing malware in a controlled environment to observe runtime behavior. |
| **Enumeration** | The process of actively extracting usernames, machine names, shares, and services from a system after initial scanning. |
| **Footprinting** | The process of accumulating data about a specific target environment, usually the first step of an attack lifecycle. |
| **Hashing** | A one-way function converting input data into a fixed-size digest, used for integrity verification. |
| **Honeypot** | A decoy system designed to attract and log attacker activity for detection/research purposes. |
| **IAM** | Identity and Access Management — the framework of policies controlling resource access in cloud environments. |
| **IDS Evasion** | Techniques (fragmentation, decoys, timing) used to avoid detection by intrusion detection systems during scanning. |
| **IDS/IPS** | Intrusion Detection/Prevention System — monitors (and optionally blocks) network traffic for malicious activity. |
| **IoT** | Internet of Things — network-connected physical devices with embedded sensors/computing. |
| **Kerberoasting** | Requesting service tickets (TGS) for SPNs and cracking them offline to recover service account passwords. |
| **LOLBin** | Living-off-the-Land Binary — a legitimate OS utility abused by attackers to evade detection. |
| **Log4Shell** | CVE-2021-44228 — a critical RCE vulnerability in Apache Log4j via JNDI lookup injection. |
| **MAC Flooding** | Overloading a switch's CAM table with fake MAC addresses, forcing it into hub-like broadcast mode. |
| **MDM** | Mobile Device Management — centralized policy enforcement and control for mobile fleets. |
| **MITM** | Man-in-the-Middle — an attacker positioned between two communicating parties to intercept/alter traffic. |
| **OS Fingerprinting** | Identifying the target's operating system based on TCP/IP stack behavior. |
| **OSINT** | Open Source Intelligence — information collected from publicly available sources. |
| **OT** | Operational Technology — hardware/software controlling physical industrial processes (ICS/SCADA). |
| **OWASP Top 10** | The industry-standard awareness list of the ten most critical web application security risks. |
| **PKI** | Public Key Infrastructure — the framework of certificates, CAs, and policies enabling trusted key exchange. |
| **Parameterized Query** | A query construction method that separates SQL code from user-supplied data, preventing injection. |
| **Passive Reconnaissance** | Gathering information without directly interacting with the target's systems (e.g., WHOIS, search engines). |
| **Persistence** | Techniques ensuring continued access to a compromised system across reboots/credential changes. |
| **Phishing** | Fraudulent communication, typically email, designed to trick a victim into revealing sensitive data or executing malware. |
| **Port Scanning** | The technique of probing a host for open TCP/UDP ports to identify running services. |
| **Pretexting** | Creating a fabricated scenario to engage a target and extract information. |
| **Privilege Escalation** | Techniques used to gain higher-level permissions than originally granted. |
| **Privilege Escalation (Cloud)** | Exploiting misconfigured IAM policies to gain permissions beyond those intended. |
| **Promiscuous Mode** | A NIC mode that captures all traffic on a segment, not just traffic addressed to it. |
| **RAT** | Remote Access Trojan — malware providing an attacker remote control over a compromised host. |
| **RCE** | Remote Code Execution — a vulnerability class allowing an attacker to execute arbitrary code on a target system. |
| **Risk** | The likelihood of a threat exploiting a vulnerability multiplied by resulting impact. |
| **Rules of Engagement (RoE)** | A formal document defining scope, timing, and constraints of an authorized penetration test. |
| **S3 Bucket** | AWS's object storage container; a common source of data breaches when misconfigured as public. |
| **SNMP Community String** | A password-like value used to authenticate to SNMP-managed devices. |
| **SQL Injection** | Insertion of malicious SQL statements into an input field to manipulate backend database queries. |
| **Sandbox Analysis** | Executing a suspicious file in an isolated environment to observe its behavior safely. |
| **Session Fixation** | Forcing a victim to use a known session ID that the attacker can then hijack. |
| **Session Hijacking** | Exploiting a valid session token to impersonate a legitimate authenticated user. |
| **Social Engineering** | Psychological manipulation of people into performing actions or divulging confidential information. |
| **Spidering/Crawling** | Automated discovery of an application's pages, parameters, and endpoints. |
| **Static Analysis** | Examining malware code/structure without executing it. |
| **Symmetric vs Asymmetric Encryption** | Symmetric uses one shared key for encrypt/decrypt (fast, e.g., AES); asymmetric uses a public/private key pair (e.g., RSA). |
| **Threat** | Any circumstance/event with potential to adversely impact an asset. |
| **Vulnerability** | A weakness that can be exploited by a threat to cause harm. |
| **WPA3-SAE** | Simultaneous Authentication of Equals — WPA3's password-authenticated key exchange, resistant to offline dictionary attacks. |
| **Zone Transfer (AXFR)** | A DNS mechanism to replicate zone data between servers; misconfiguration can leak entire DNS records to attackers. |