# 📋 Changelog

All notable repository changes are recorded here. This changelog distinguishes documentation and repository maintenance from application capabilities.

## [Unreleased]

### Documentation
- Rebuilt the main README with a complete project overview, snapshot, scope, workflow, architecture, technology direction, repository map, status, setup guidance, safety requirements and documentation index.
- Expanded the documentation landing page and recommended reading paths.
- Expanded clinical safety, architecture, API, database, installation, development, testing, deployment, operations, privacy, security, FAQ and troubleshooting guidance.
- Clarified that all future product capabilities are planned and not currently implemented.

### Repository maintenance
- Added a root `.gitignore` covering environment secrets, logs, editor files, caches and common build outputs.
- Added structured GitHub issue forms for bug reports, feature requests and documentation improvements, plus issue contact configuration.
- Added a documentation-focused GitHub Actions workflow that checks required files, non-empty Markdown files and relative Markdown links.
- Added weekly Dependabot checks for GitHub Actions dependencies.
- Updated the README repository tree and documented the scope of each automation workflow.
- Retained direct-to-main repository maintenance.

### Limitations
- CodeQL is deferred until application source code exists; running a source-code analyzer against a documentation-only repository would provide no meaningful coverage.
- Funding configuration was not added because no verified sponsorship destination was provided.

### Limitations
- No frontend, backend, OCR, model, clinical rules engine, database, API, automated test suite or production deployment has been added.
- No clinical validation or regulatory compliance claim is made.
