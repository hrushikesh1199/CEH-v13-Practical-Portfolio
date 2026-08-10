# Module 20 — Cryptography

## Overview
Applied cryptography covering hashing, encryption, PKI/certificate management, and disk encryption, closing out the CEH v13 curriculum.

## Learning Objectives
- Perform multi-layer hashing analysis using CyberChef
- Perform file/text encryption using CryptoForge
- Create and deploy self-signed X.509 certificates
- Implement full-disk encryption using VeraCrypt
- Apply AI-assisted cryptographic technique analysis using ShellGPT

## Labs Completed
- Lab 1.1 — Multi-layer Hashing using CyberChef
- Lab 1.2 — File and Text Message Encryption using CryptoForge
- Lab 2 — Create and Use Self-signed Certificates
- Lab 3 — Disk Encryption using VeraCrypt
- Lab 4 — Cryptographic Techniques using ShellGPT

## Tools & Technologies
- CyberChef
- CryptoForge
- OpenSSL
- VeraCrypt

## Key Commands / Techniques
```bash
openssl req -x509 -newkey rsa:4096 -keyout key.pem -out cert.pem -days 365 -nodes
openssl dgst -sha256 file.txt
veracrypt --create /path/to/volume --size=10G --encryption=AES --hash=SHA-512
```

## Sample Payloads / Test Strings
```
N/A for this module.
```
> All commands and payloads above were executed strictly within EC-Council's isolated CEH iLabs cyber range against consenting lab targets, for educational and certification purposes only.

## Detection & Mitigation
- Use only vetted, modern algorithms (AES-256, SHA-256/512, RSA-2048+ or ECC)
- Never roll custom cryptography; rely on audited libraries (OpenSSL, libsodium)
- Implement proper key management/rotation and use HSMs for high-value keys
- Enforce TLS 1.2+ across all services and disable deprecated ciphers (RC4, 3DES, SSLv3)
- Encrypt data at rest (full-disk/volume encryption) and in transit uniformly

## Key Definitions
| Term | Definition |
|---|---|
| **Hashing** | A one-way function converting input data into a fixed-size digest, used for integrity verification. |
| **PKI** | Public Key Infrastructure — the framework of certificates, CAs, and policies enabling trusted key exchange. |
| **Symmetric vs Asymmetric Encryption** | Symmetric uses one shared key for encrypt/decrypt (fast, e.g., AES); asymmetric uses a public/private key pair (e.g., RSA). |

## References / Sources
- NIST FIPS 140-3
- OWASP Cryptographic Storage Cheat Sheet
- EC-Council CEH v13 Module 20

---
[⬅ Back to main README](../../README.md)
