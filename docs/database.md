# 🗄️ Database and Persistence

## Current status

No database engine, schema, migration, or persistence layer is currently implemented.

## Data modelling principles

Before selecting a database, define the minimum information needed for the intended workflow. Potential data categories include:

- User and professional identity references.
- Prescription input metadata.
- Extracted candidate values and source locations.
- Human-confirmed structured values.
- Rule and reference-source versions.
- Review findings and unresolved items.
- Professional review actions.
- Security and access audit events.

These are conceptual categories, not existing database tables.

## Privacy and access controls

- Establish ownership and tenant boundaries.
- Apply least-privilege roles and server-side authorization.
- Encrypt sensitive data in transit and at rest.
- Avoid storing original uploads unless there is a documented need.
- Keep audit events separate from debug logs.
- Do not store raw prompts or full model responses by default.
- Define retention, correction, export and deletion behavior before collecting records.

## Reliability

If persistence is introduced, document migration, rollback, backup, restoration, encryption key management, recovery objectives and backup expiry. Test restoration rather than assuming backups are usable.

## Development data

Use synthetic fixtures by default. Any use of de-identified data requires documented authorization and a re-identification risk assessment. Never commit patient data or production database exports.
