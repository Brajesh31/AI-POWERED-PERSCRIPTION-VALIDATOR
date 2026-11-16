# 🧪 Testing Strategy

## Current status

No automated test suite or application implementation is present. There is no test coverage, build result, or clinical validation claim.

## Planned test layers

| Test layer | Required coverage | Example cases |
|---|---|---|
| Unit tests | Parsing, normalization, conversion and individual deterministic rules | Missing values, known formats, invalid types |
| Schema tests | Accepted and rejected request shapes | Missing keys, unexpected keys, malformed payloads |
| Boundary tests | Numeric, date, unit and file boundaries | Empty fields, extreme values, unsupported units |
| Integration tests | Authentication, persistence and provider adapters | Unauthorized access, timeout, unavailable source |
| Security tests | Access control, uploads, injection and data leakage | Oversized files, malicious content, cross-user access |
| Resilience tests | Safe behavior under dependency failure | Stale data, malformed response, network timeout |
| Workflow tests | Human confirmation and professional review | Ambiguous extraction, unresolved findings |
| Usability tests | Safe interpretation of results | Preventing advisory flags from being mistaken for approval |

## Synthetic test data

Use synthetic fixtures by default. Do not commit real prescriptions, patient records, scanned documents or unredacted model prompts. De-identified datasets require documented approval and re-identification risk assessment.

## Clinical validation is separate

Passing software tests does not establish clinical accuracy or safety. Clinical rules need qualified professional review. The complete workflow also requires appropriate risk analysis, usability evaluation, and validation against the intended use.

## Reporting test results

Record the command, runtime version, test scope, pass/fail result, and known gaps. Never claim full coverage when only a subset of services or rules has been exercised.
