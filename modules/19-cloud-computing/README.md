# Module 19 — Cloud Computing

## Overview
Cloud-native attack surface across Azure and AWS, including identity reconnaissance, storage misconfiguration exploitation, IAM privilege escalation, and container image vulnerability assessment.

## Learning Objectives
- Perform Azure AD/Entra ID reconnaissance using AADInternals
- Identify and exploit publicly exposed AWS S3 buckets
- Escalate IAM user privileges via misconfigured policies
- Perform vulnerability assessment on Docker images using Trivy

## Labs Completed
- Lab 1 — Azure Reconnaissance with AADInternals
- Lab 2 — Exploit Open S3 Buckets Using AWS CLI
- Lab 3 — Escalate IAM User Privileges via Misconfigured Policy
- Lab 4 — Vulnerability Assessment on Docker Images Using Trivy

## Tools & Technologies
- AADInternals (PowerShell)
- AWS CLI
- Trivy
- ScoutSuite / Prowler (cloud posture)

## Key Commands / Techniques
```bash
Invoke-AADIntReconAsOutsider -DomainName target.com   # Azure tenant recon
aws s3 ls s3://target-bucket --no-sign-request         # test public bucket access
aws iam simulate-principal-policy --policy-source-arn <arn> --action-names s3:GetObject
trivy image myapp:latest
```

## Sample Payloads / Test Strings
```
N/A for this module.
```
> All commands and payloads above were executed strictly within EC-Council's isolated CEH iLabs cyber range against consenting lab targets, for educational and certification purposes only.

## Detection & Mitigation
- Enforce S3 Block Public Access at the account level; audit bucket policies regularly
- Apply least-privilege IAM policies and enable IAM Access Analyzer
- Enable Conditional Access and MFA on Azure AD/Entra ID; restrict legacy authentication
- Scan container images in CI/CD with Trivy/Grype before registry push
- Enable cloud-native logging (CloudTrail, Azure Monitor) with SIEM integration

## Key Definitions
| Term | Definition |
|---|---|
| **IAM** | Identity and Access Management — the framework of policies controlling resource access in cloud environments. |
| **S3 Bucket** | AWS's object storage container; a common source of data breaches when misconfigured as public. |
| **Privilege Escalation (Cloud)** | Exploiting misconfigured IAM policies to gain permissions beyond those intended. |

## References / Sources
- AWS Well-Architected Framework — Security Pillar
- Microsoft Entra ID Security Documentation
- EC-Council CEH v13 Module 19

---
[⬅ Back to main README](../../README.md)
