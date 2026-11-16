# API design principles

## Current status

No API server, endpoint, request schema, or response schema is implemented. The following is a design checklist, not a live API contract.

## Future contract requirements

For every endpoint document:
- Purpose, authentication, authorization, and data classification.
- Request schema, supported content types, size limits, and validation behavior.
- Response schema, stable error codes, and correlation identifiers.
- Idempotency, pagination, rate limits, and timeout behavior where relevant.
- Audit events and retention implications.

## Safety semantics

A response must distinguish between extraction, deterministic checks, advisory flags, and professional review. It must not return a single unqualified `valid: true` result that implies medical safety.

Represent unresolved or ambiguous findings explicitly. Include rule/source identifiers and versions for clinical flags. Never expose model chain-of-thought or treat model confidence as clinical evidence.

## Example error categories

- `UNSUPPORTED_INPUT`
- `MALFORMED_REQUEST`
- `REQUIRED_FIELD_MISSING`
- `AMBIGUOUS_EXTRACTION`
- `REFERENCE_DATA_UNAVAILABLE`
- `REVIEW_REQUIRED`
- `INTERNAL_ERROR`

Examples must use synthetic data only.
