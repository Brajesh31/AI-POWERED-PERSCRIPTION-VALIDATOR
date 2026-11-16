# 🔒 Privacy and Data Lifecycle

Prescription records may contain sensitive personal and health information. Treat inputs, extracted text, model prompts and outputs, caches, analytics events, audit records and backups as potentially sensitive.

## Data minimization

- Define the purpose and lawful basis before collecting data.
- Collect only the fields needed for the documented workflow.
- Prefer synthetic data for examples, development and tests.
- Use de-identified data only after approval and re-identification risk assessment.
- Do not send patient information to an external model or OCR provider without documented privacy, security and contractual approval.

## Lifecycle requirements

Document collection, access, transfer, processing, storage, retention, export, correction, deletion, backup expiry and incident handling. Define retention periods for each data category. Do not keep records indefinitely by default.

## Technical requirements

- Encrypt data in transit and at rest.
- Enforce server-side authorization and least privilege.
- Separate development, staging and production data.
- Keep secrets in a managed secret store.
- Use opaque request identifiers in logs.
- Redact patient content from errors, traces and analytics.
- Restrict and audit access to records and backups.

## External processing

Before using a third-party provider, document what data leaves the system, the provider's purpose, retention and training terms, geographic processing, subprocessors, deletion controls and contractual protections.

## Governance

Before production, identify applicable privacy laws, controller/processor responsibilities, data residency, breach notification duties, and access or deletion request procedures. This document is engineering guidance, not a legal compliance determination.
