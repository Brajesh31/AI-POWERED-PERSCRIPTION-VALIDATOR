# 🗺️ Roadmap

This roadmap describes proposed milestones. A planned item must not be described as implemented until code, tests and review evidence exist.

## Phase 1: Intended use and governance
- [ ] Define intended use, target users and explicit exclusions.
- [ ] Assign clinical, privacy, security and regulatory review ownership.
- [ ] Define target deployment jurisdictions and applicable requirements.
- [ ] Identify supported prescription formats and data-minimization needs.
- [ ] Evaluate authoritative, licensed clinical reference sources.

## Phase 2: Technical foundation
- [ ] Select the technology stack based on approved requirements.
- [ ] Define identity, authentication and authorization.
- [ ] Define audit, retention and deletion boundaries.
- [ ] Add reproducible dependency management and CI.
- [ ] Establish synthetic fixtures and baseline security tests.

## Phase 3: Structured intake
- [ ] Implement strict file type and size validation.
- [ ] Add a narrow, documented extraction workflow.
- [ ] Preserve page and text provenance.
- [ ] Require human confirmation for uncertain fields.
- [ ] Normalize units and identifiers without guessing.

## Phase 4: Deterministic checks
- [ ] Define versioned validation rules with qualified review.
- [ ] Add unit, boundary, integration and regression tests.
- [ ] Keep missing, ambiguous and conflicting inputs unresolved.
- [ ] Record the rule and reference versions used for each finding.

## Phase 5: Professional review experience
- [ ] Build a secure reviewer interface.
- [ ] Separate extraction output, rule findings and advisory information.
- [ ] Add explicit professional review and audit workflows.
- [ ] Conduct usability assessment for automation-bias risks.

## Phase 6: Optional AI assistance
- [ ] Evaluate whether an AI component is necessary for the intended use.
- [ ] Isolate the provider behind a replaceable adapter.
- [ ] Prevent model output from making clinical decisions or invoking privileged actions.
- [ ] Assess provider privacy, retention and security terms.

## Phase 7: Release readiness
- [ ] Complete clinical risk analysis and validation.
- [ ] Complete privacy and security reviews.
- [ ] Assess applicable regulatory obligations.
- [ ] Test incident response, backup, restore and rollback.
- [ ] Approve only a clearly defined and appropriately validated intended use.

## Release gate

No clinical or patient-facing release until qualified reviewers approve the intended use, safety controls, validation evidence, privacy and security controls, and deployment readiness.
