# Architecture proposal

## Status

This is a conceptual architecture only. No corresponding services or modules are currently implemented in this repository.

## Suggested processing boundaries

1. **Input boundary:** accept only explicitly supported formats and reject oversized or unsupported files.
2. **Identity and consent:** authenticate the operator, authorize the action, and establish a lawful purpose before processing sensitive information.
3. **Extraction:** parse structured data or extract candidate text. Preserve source coordinates and provenance where possible.
4. **Normalization:** normalize units and identifiers using explicit, versioned mappings. Never silently guess missing values.
5. **Deterministic checks:** execute reviewed, versioned rules for required fields, data types, ranges, and consistency.
6. **Evidence-backed review assistance:** consult only validated, maintained clinical knowledge sources. Record their version and retrieval date.
7. **Human review:** present flags, source evidence, limitations, and unresolved questions to a qualified professional.
8. **Audit and retention:** record access and actions without copying unnecessary patient data into logs.

## Non-negotiable boundaries

- A language model must not be the authority for clinical facts or medication recommendations.
- A model must not autonomously approve, reject, prescribe, change, or dispense medication.
- Missing, ambiguous, conflicting, stale, or unavailable data must produce an explicit unresolved state.
- Every clinical flag must be traceable to a rule or source and its version.
- The system must remain usable and safe when any external AI provider is unavailable.

## Future architecture decision records

Before implementation, record decisions for supported input types, deployment boundary, identity provider, clinical knowledge source, persistence, audit strategy, and model-provider isolation.
