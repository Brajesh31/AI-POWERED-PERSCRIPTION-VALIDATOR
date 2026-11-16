# 🧑‍💻 Development Workflow

## Current status

The repository has no application code, dependency manifest, or automated test suite. This guide defines expectations for future engineering work.

## Engineering principles

- Keep clinical rules deterministic, versioned and independently testable.
- Separate extraction, human confirmation, normalization, rule evaluation, AI assistance and professional review.
- Use explicit data schemas and units.
- Isolate external providers behind replaceable interfaces.
- Treat documents and extracted text as untrusted input.
- Make timeouts, malformed output, stale data and ambiguity visible.
- Fail safely. Never convert a technical failure into a successful clinical result.

## Change workflow

1. Describe the problem and intended user behavior.
2. Identify privacy, security and clinical safety implications.
3. Agree on the data contract and failure states.
4. Implement the smallest focused change.
5. Add tests using synthetic fixtures.
6. Update relevant documentation and the changelog.
7. Run applicable static checks, tests and build commands.
8. Request qualified clinical review for changes affecting clinical behavior.

## Pull request expectations

A pull request should describe the change, motivation, affected components, test commands and results, risks, and known limitations. Include screenshots only when they contain no sensitive data.

Never commit patient records, prescription images, credentials, raw provider prompts, generated caches, or unreviewed clinical datasets.
