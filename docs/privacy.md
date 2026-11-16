# Privacy and data lifecycle

Prescription records may contain sensitive personal and health information. Treat all inputs, extracted text, model prompts, model outputs, caches, analytics events, and backups as potentially sensitive.

## Data minimization

- Define the purpose and lawful basis before collecting data.
- Collect only fields required for the documented workflow.
- Prefer synthetic data for examples and tests.
- De-identify data before non-production use and assess re-identification risk.
- Do not send patient information to external model providers unless an approved, documented privacy and contractual review permits it.

## Lifecycle controls

Document collection, access, transfer, storage, retention, export, correction, deletion, backup expiry, and incident handling. Define retention periods rather than keeping records indefinitely.

## Technical controls

Use encryption in transit and at rest, role-based least privilege, strong authentication, access logs, secure secret storage, and environment separation. Logs should use opaque request identifiers and avoid raw prescription contents.

## User rights and governance

Before production, identify applicable privacy laws, data-controller/processor responsibilities, vendor terms, data residency requirements, breach notification duties, and procedures for access or deletion requests. This document is guidance, not a legal compliance determination.
