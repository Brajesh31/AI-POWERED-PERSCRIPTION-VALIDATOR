# 🧯 Operations and Incident Response

## Current status

No application services, production deployment, clinical workflow, or operational monitoring are present. This guide sets expectations for future deployments.

## Events requiring procedures

A future operating plan should cover:
- Suspected exposure of patient or prescription data.
- Unauthorized record access or account compromise.
- Incorrect or unexpected extraction output.
- Reference data that is unavailable, stale, or changed.
- Parsing or deterministic-rule regression.
- External AI provider outage or suspicious model output.
- Audit storage failure or missing audit events.
- Backup, restoration, and deletion failures.

## Incident response sequence

1. Protect patients and users. Disable affected functionality if safe operation cannot be assured.
2. Notify accountable security, privacy, and clinical owners.
3. Preserve necessary evidence without copying unnecessary patient content.
4. Assess the affected services, time range, records and possible impact.
5. Follow applicable contractual and legal notification obligations.
6. Contain, remediate and test the underlying issue.
7. Document the incident, decisions and corrective actions.
8. Resume service only after authorized review.

## Operational controls

- Define on-call ownership and escalation paths.
- Monitor service health without capturing sensitive payloads.
- Restrict access to audit and incident records.
- Define log and audit retention separately.
- Test backups and recovery procedures.
- Keep rollback instructions and dependency ownership current.

Do not use public GitHub issues for sensitive incident details.
