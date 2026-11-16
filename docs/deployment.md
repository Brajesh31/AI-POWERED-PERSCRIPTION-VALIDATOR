# 🚀 Deployment Readiness

## Current status

No application runtime, container image, infrastructure configuration, or production deployment exists in this repository. It must not be deployed for patient-facing or clinical use.

## Release prerequisites

| Area | Required evidence |
|---|---|
| Intended use | Defined users, purpose, exclusions and accountable owner |
| Clinical safety | Risk analysis, reviewed rules and qualified clinical oversight |
| Privacy | Data-flow map, lawful basis, retention and deletion process |
| Regulatory | Applicable jurisdictional assessment |
| Identity | Authentication, authorization and least privilege |
| Secrets | Managed credentials with rotation procedures |
| Transport and storage | TLS and encryption at rest |
| AI providers | Approved data-processing terms and restricted data transfer |
| Audit | Restricted access logs and defined retention |
| Reliability | Backup, restore, monitoring and incident response |
| Validation | Software, security, usability and clinical evidence |
| Release management | Rollback plan and authorized release approval |

## Infrastructure principles

When implementation begins, isolate environments, restrict network access, store secrets outside source control, avoid sensitive payloads in logs, and use health checks that do not expose patient information.

## Go-live rule

Do not deploy clinical or patient-facing functionality until the accountable clinical, security, privacy, and regulatory reviewers have approved the intended use and supporting evidence. A successful software build is not clinical clearance.
