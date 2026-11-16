# 📚 AI-Powered Prescription Validator Documentation

This documentation describes the current repository foundation, proposed architecture, safety boundaries, and engineering expectations for AI-Powered Prescription Validator.

Start with the [main README](../README.md) for the project overview and status. The project currently has no runnable application, model, API, database, or clinical validation engine. Documentation describing future capabilities is explicitly a proposal, not proof that a feature exists.

## Documentation Map

| Guide | Purpose |
|---|---|
| [Project Status](project-status.md) | Verified current state and implementation gaps |
| [Architecture](architecture.md) | Proposed system layers and trust boundaries |
| [Clinical Safety](clinical-safety.md) | Clinical risks, hazard controls and human review |
| [API Design](api.md) | Future API contracts and safe response semantics |
| [Database](database.md) | Persistence, audit, retention and deletion requirements |
| [Development](development.md) | Engineering practices and change workflow |
| [Installation](installation.md) | Current installation status and future setup requirements |
| [Testing](testing.md) | Unit, integration, security and workflow testing |
| [Security](security.md) | Application and AI-specific security requirements |
| [Privacy](privacy.md) | Sensitive data lifecycle and external processing |
| [Deployment](deployment.md) | Production readiness gates |
| [Operations](operations.md) | Incident response and operational requirements |
| [Troubleshooting](troubleshooting.md) | Safe issue reporting and future diagnostics |
| [FAQ](faq.md) | Common questions about capability and intended use |

## Recommended Reading

### First-time readers
1. Read the [main README](../README.md).
2. Confirm the actual [project status](project-status.md).
3. Review [clinical safety](clinical-safety.md) and [privacy](privacy.md).
4. Read the [architecture proposal](architecture.md).

### Engineering contributors
1. Read [development](development.md).
2. Review [API design](api.md) and [database guidance](database.md).
3. Follow the [testing strategy](testing.md).
4. Update the relevant documentation with every implementation change.

### Security and deployment reviewers
1. Review [security controls](security.md).
2. Review [privacy and data lifecycle](privacy.md).
3. Review [operations and incident response](operations.md).
4. Complete the [deployment readiness](deployment.md) checklist.

## Documentation Rules

- Describe implemented behavior only when code and tests support it.
- Label design proposals and roadmap items as planned.
- Do not publish real patient information, prescription images, credentials, or unredacted logs.
- Cite the version and provenance of any future clinical reference source.
- Keep limitations and unresolved risks visible.

## Important

Documentation does not make this repository clinically validated or production-ready. Any future clinical-facing release requires qualified professional review, safety validation, privacy and security assessment, and applicable regulatory review.
