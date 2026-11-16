# Clinical safety requirements

## Intended role

The proposed software may assist a qualified healthcare professional by organizing information and identifying items requiring attention. It must not replace professional judgment.

## Hazard controls

| Hazard | Required control |
|---|---|
| Incorrect text extraction | Show extracted values with source context; require confirmation for uncertain fields |
| Wrong medicine or strength match | Use controlled identifiers and explicit ambiguity handling |
| Missing dose or route | Never infer; mark unresolved and require human review |
| Incorrect unit conversion | Use tested, versioned conversion functions and preserve original units |
| Unsupported interaction flag | Cite the exact evidence source and version; allow clinician review |
| Model hallucination | Do not use free-form model output as a clinical rule or source of truth |
| Stale reference data | Track source version and update date; surface stale or unavailable data |
| Automation bias | Display limitations and uncertainty; require a named professional decision |
| Service failure | Fail closed for clinical approval; never imply validation succeeded |

## Required workflow semantics

Use distinct states such as `not_started`, `needs_review`, `unable_to_assess`, and `reviewed_by_professional`. Do not use a single green “valid” state that could be interpreted as clinical approval.

## Validation before use

Clinical rules, terminology mappings, and data sources must be reviewed by qualified domain experts. Risk analysis, usability testing, and applicable regulatory assessment are prerequisites for any real-world clinical deployment.
