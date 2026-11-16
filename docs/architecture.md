# 🏗️ Proposed Architecture

## Status

This is a design proposal only. The repository does not currently contain a frontend, backend, extraction pipeline, rules engine, model, or database.

## Design goals

- Separate document extraction from confirmed prescription information.
- Keep deterministic checks independent from generative AI.
- Preserve provenance for every extracted or normalized field.
- Make ambiguous, missing, stale and unavailable data explicit.
- Require professional review for clinical decisions.
- Minimize sensitive data movement and retention.

## Proposed processing layers

| Layer | Responsibility | Trust boundary |
|---|---|---|
| Review interface | Capture input and present findings | Authenticated professional |
| Application API | Authorization, request validation and orchestration | Server-side policy |
| Intake adapter | File type, size and content validation | Untrusted uploaded file |
| Extraction adapter | OCR or structured extraction | Candidate text, not confirmed data |
| Confirmation layer | Professional confirms uncertain fields | Human-confirmed field values |
| Normalization | Units, medicine identifiers and structured fields | Versioned mappings, no guessing |
| Deterministic rules | Required-field and consistency checks | Tested, versioned rule set |
| Reference adapter | Approved clinical evidence lookup | Source provenance and freshness |
| Optional AI adapter | Summarization or organization assistance | Untrusted advisory output |
| Review workflow | Professional interpretation and decision | Human accountability |
| Audit and persistence | Minimum necessary data and review events | Restricted access and retention |

## Processing flow

```text
Authenticated reviewer
        |
        v
Secure intake and file validation
        |
        v
Extraction of candidate fields
        |
        v
Human confirmation of uncertain values
        |
        v
Versioned normalization
        |
        v
Deterministic checks + approved reference lookup
        |
        v
Review findings with evidence and limitations
        |
        v
Qualified professional review
        |
        v
Restricted audit record
```

## AI provider boundary

AI calls, if introduced, must be isolated behind an adapter. The application must validate all model outputs against strict schemas and treat them as untrusted. A model must not invoke privileged tools, bypass authorization, update a prescription, or approve a clinical action.

## Resilience

If OCR, a model provider, reference data, storage, or another dependency is unavailable, the system must return an explicit unresolved state. A technical failure must never be represented as successful validation.

## Decisions required before implementation

Select supported input formats, intended users, identity provider, clinical data sources, persistence approach, hosting jurisdiction, audit and retention model, and technology stack. Record material choices as architecture decision records.
