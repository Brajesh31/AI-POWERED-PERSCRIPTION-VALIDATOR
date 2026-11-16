# 🛡️ Clinical Safety Requirements

## Purpose and status

This document defines safety requirements for a future prescription-review application. No clinical software or validation engine is implemented in this repository. These requirements are not evidence of clinical validation.

## Intended role

The proposed software may assist an appropriately qualified healthcare professional by organizing prescription details and surfacing items that require attention. It must not replace professional judgment or authorize treatment.

## Hazard and control register

| Potential hazard | Required mitigation |
|---|---|
| Incorrect OCR or text extraction | Preserve source context, highlight uncertain fields, require confirmation |
| Wrong medicine or strength match | Use controlled identifiers and explicit ambiguity handling |
| Missing dose, route or frequency | Never infer missing information; mark unresolved |
| Incorrect unit conversion | Use reviewed, tested and versioned conversion functions |
| False interaction or contraindication alert | Cite validated evidence and source version; require professional interpretation |
| Missing clinical warning | Do not claim comprehensive safety assessment; disclose source coverage |
| Hallucinated model response | Never treat free-form AI output as a clinical rule or source of truth |
| Stale clinical reference | Record update date and version; surface stale or unavailable data |
| Automation bias | Avoid generic “safe/valid” indicators; require explicit professional review |
| Provider or database failure | Fail visibly and preserve an unresolved state |
| Unauthorized record access | Enforce server-side authorization and access audit |

## Required workflow states

Future software should clearly distinguish states such as:

- `not_started`
- `input_received`
- `needs_field_confirmation`
- `checks_incomplete`
- `needs_professional_review`
- `unable_to_assess`
- `reviewed_by_professional`

Do not use one positive boolean such as `valid: true` to imply clinical safety.

## Professional accountability

A qualified clinician or pharmacist must make the clinical decision. The application must not independently approve, reject, prescribe, change, or dispense medication. Record professional review actions without implying that a software flag is a clinical judgment.

## Validation before any use

Before real-world use, establish intended use, risk management, clinical ownership, evidence sources, usability evaluation, security and privacy controls, and applicable regulatory assessment. Reviewers must be suitably qualified for the relevant clinical domain and jurisdiction.
