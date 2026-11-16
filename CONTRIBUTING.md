# 🤝 Contributing

Thank you for considering a contribution to AI-Powered Prescription Validator.

## Current project state

The repository is a documentation foundation. It does not yet contain a runnable application, model, API, database, or test suite. Contributions should not describe planned capabilities as existing functionality.

## Contribution principles

- Keep changes focused and explain the problem being solved.
- Preserve the distinction between extraction, deterministic checks, AI assistance and professional review.
- Do not introduce autonomous prescription approval, rejection, modification, or dispensing.
- Do not invent missing medicine, strength, dose, route, frequency or duration values.
- Use synthetic examples and fixtures.
- Treat patient information and prescription documents as sensitive.
- Document limitations, assumptions, dependencies and evidence.

## Suggested workflow

1. Review the README and relevant guides in [docs/](docs/README.md).
2. Open or review an issue describing the proposed change.
3. Create a focused branch.
4. Implement the change with tests where code exists.
5. Run the checks relevant to the changed component.
6. Update documentation and [CHANGELOG.md](CHANGELOG.md).
7. Submit a pull request with validation results and known limitations.

## Pull request expectations

A pull request should describe the change, motivation, affected components, test commands and results, risks, and known limitations. Never commit patient records, prescription images, credentials, raw provider prompts, generated caches, or unreviewed clinical datasets.

- [ ] The change has a clear purpose and scope.
- [ ] Documentation reflects actual behavior.
- [ ] Tests are included or the reason for their absence is stated.
- [ ] No secrets or patient information are committed.
- [ ] Security, privacy and clinical implications are described.
- [ ] Unimplemented work is not presented as complete.

Changes affecting clinical interpretation require qualified professional review before any clinical release.

See [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) for community expectations.
