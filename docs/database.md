# Database and persistence

## Current status

No database engine, schema, migration, or persistence layer is implemented.

## Future design checklist

If persistence is required, define:
- Entities, relationships, ownership, and tenant boundaries.
- Minimum necessary patient and prescription fields.
- Encryption, key management, and access-control strategy.
- Audit events separate from application debug logs.
- Retention, correction, export, and deletion semantics.
- Backup encryption, restore testing, and expiry.
- Schema migration and rollback process.
- Data lineage for extracted values, rules, and reference sources.

Avoid storing raw uploads or model prompts by default. Establish a documented purpose and retention period for each stored field. Use synthetic fixtures for tests and migrations.
