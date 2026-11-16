# Security controls

## Sensitive assets

Treat uploaded files, prescription text, patient identifiers, clinical flags, audit records, credentials, and provider responses as sensitive assets.

## Minimum controls for a future implementation

- Authentication and server-side authorization on every sensitive operation.
- Least-privilege service identities and separate development, staging, and production environments.
- Secret-manager-backed credentials; no secrets in source, logs, fixtures, or client bundles.
- TLS for network traffic and encryption at rest for stored sensitive data.
- File type, size, content, and malware checks at upload boundaries.
- Input validation, output encoding, safe error messages, and dependency vulnerability management.
- Rate limits and abuse monitoring for exposed endpoints.
- Audit events for access and actions, with restricted access and defined retention.
- Backups, restore tests, incident response, and secure deletion processes.

## AI-specific threats

Treat uploaded documents and extracted text as untrusted input. Defend against prompt injection, data exfiltration, insecure tool invocation, model-provider leakage, and unsafe reliance on generated output. AI output must not bypass deterministic authorization or clinical review controls.

## Reporting

Report suspected vulnerabilities privately to the repository maintainer. Do not include real patient data in a report. Provide affected component, reproduction steps using synthetic data, impact, and suggested mitigation.
