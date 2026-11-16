# 🔐 Security Controls

## Security status

This repository contains no application code or deployed service, so there are no implemented application security controls to certify. The following controls are prerequisites for a future implementation.

## Sensitive assets

Treat prescription documents, extracted text, patient identifiers, review findings, audit records, credentials, provider responses and backups as sensitive assets.

## Minimum application controls

- Authentication and server-side authorization on every sensitive operation.
- Least-privilege roles and service identities.
- Managed credentials, rotation and separate environment secrets.
- TLS for network communication and encryption at rest.
- File extension, MIME type, content, size and malware checks at upload boundaries.
- Strict request schemas, safe output handling and bounded processing.
- Rate limits, abuse monitoring and safe error responses.
- Audit events for access and professional actions.
- Dependency, container and supply-chain security checks.
- Backup, restore, incident response and secure deletion procedures.

## AI-specific security

Treat uploaded files, OCR text and user-supplied content as untrusted. Plan controls for prompt injection, data exfiltration, insecure tool invocation, model-provider leakage, malicious files and unsafe reliance on generated content. Model output must never bypass authorization or clinical review.

## Secrets

Never commit API keys, passwords, access tokens, patient records, prescription images, database exports or private provider logs. A secret deleted from the latest commit may remain in Git history. Revoke or rotate it with the issuer.

## Vulnerability reporting

Report suspected vulnerabilities privately to the repository maintainer. Do not include real patient data. Provide the affected component, synthetic reproduction steps, impact and suggested mitigation.
