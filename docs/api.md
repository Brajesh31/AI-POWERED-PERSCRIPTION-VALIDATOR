# 🔌 API Design

## Current status

No API server, route, request schema, or response schema exists in this repository. This page defines requirements for a future API, not a live contract.

## Contract requirements

Every future endpoint must document:

- Purpose and intended caller.
- Authentication and server-side authorization.
- Input schema, content type, supported file formats and size limits.
- Output schema and stable error codes.
- Idempotency and retry behavior where applicable.
- Rate limits, timeout behavior and abuse controls.
- Audit event requirements and data retention impact.

## Separate processing outcomes

Do not conflate these concepts:

1. **Extraction:** candidate values found in an input.
2. **Confirmation:** values explicitly checked by a person.
3. **Deterministic checks:** results of documented software rules.
4. **Advisory flags:** items that may warrant further review.
5. **Professional review:** a decision made by a qualified person.

A future response must not reduce these stages to an unqualified `valid: true` field.

## Suggested error categories

| Code | Meaning |
|---|---|
| `UNSUPPORTED_INPUT` | File or payload format is not supported |
| `FILE_TOO_LARGE` | Upload exceeds the configured limit |
| `MALFORMED_REQUEST` | Request does not satisfy the input schema |
| `REQUIRED_FIELD_MISSING` | A required input field is absent |
| `AMBIGUOUS_EXTRACTION` | More than one candidate interpretation exists |
| `REFERENCE_DATA_UNAVAILABLE` | Required reference source cannot be reached |
| `REVIEW_REQUIRED` | Professional review is required |
| `UNABLE_TO_ASSESS` | The system cannot complete the requested check |
| `INTERNAL_ERROR` | Unexpected server-side failure |

## Security requirements

Never include patient records, prescription scans, credentials, raw prompts, or provider secrets in errors. Avoid returning internal stack traces. Use correlation identifiers for support and audit, and keep them separate from sensitive data.

Examples must use synthetic values only. Publish an OpenAPI schema only after the API is actually implemented and tested.
