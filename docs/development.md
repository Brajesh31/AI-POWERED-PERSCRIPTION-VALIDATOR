# Development workflow

## Current status
The repository does not yet include application code, a dependency manifest, or automated tests. This workflow defines expectations for future implementation.

## Engineering principles
- Keep clinical rules deterministic, versioned, independently testable, and reviewed.
- Separate document parsing, normalization, rule evaluation, model assistance, and human review.
- Isolate external provider calls behind replaceable interfaces.
- Use strict schemas and explicit units.
- Make timeouts, malformed output, ambiguous extraction, and provider outages visible.
- Fail safely and never convert a technical failure into a successful validation state.

## Change process
1. Explain the user problem and scope.
2. Identify safety, privacy, and security impact.
3. Add or update tests using synthetic fixtures.
4. Update the relevant documentation and changelog.
5. Run formatting, static analysis, tests, and build checks once those tools exist.
6. Request domain-expert review for any change affecting clinical behavior.

## Pull requests
Keep changes focused. Include test results and known limitations. Never attach patient records, prescription scans, secrets, or unredacted provider logs.
