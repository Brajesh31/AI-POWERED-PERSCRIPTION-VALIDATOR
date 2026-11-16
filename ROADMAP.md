# Roadmap

This roadmap describes possible engineering milestones. None of the planned application capabilities should be considered implemented until code, tests, and review evidence are committed.

## Phase 1: Scope and governance
- Define intended use, users, supported jurisdictions, and explicit exclusions.
- Establish clinical, privacy, security, and regulatory review ownership.
- Define supported input formats and data minimization requirements.

## Phase 2: Safe technical foundation
- Select a runtime and add reproducible dependency management.
- Define authentication, authorization, file upload limits, and audit requirements.
- Establish synthetic fixtures and baseline automated checks.

## Phase 3: Structured extraction and deterministic checks
- Implement parsing for a narrowly defined input format.
- Add field-level provenance and confidence/ambiguity handling.
- Implement versioned deterministic validation rules with expert review.
- Never infer missing dose, strength, route, frequency, or duration.

## Phase 4: Evidence-backed assistance
- Evaluate approved, versioned clinical reference sources.
- Add optional model assistance behind an isolated provider interface.
- Prevent model output from authorizing clinical decisions.

## Phase 5: Human review and validation
- Add review queues, explicit unresolved states, and auditable professional decisions.
- Conduct security, usability, risk, and clinical validation.
- Assess applicable regulatory obligations before any real-world deployment.

## Release gate
No clinical or patient-facing release until qualified reviewers approve intended use, safety controls, validation evidence, privacy and security controls, and deployment readiness.
