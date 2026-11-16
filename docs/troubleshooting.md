# Troubleshooting

## Current status
There is no executable application to troubleshoot yet. When implementation is added, record reproducible issues against the exact runtime and dependency versions.

## Recommended report format
Include the command, operating system, runtime version, sanitized configuration, expected behavior, actual behavior, and minimal reproduction using synthetic data.

## Common future failure categories
- Unsupported or oversized input: verify documented format and size limits.
- Ambiguous extraction: require field confirmation; never guess.
- Reference data unavailable or stale: return an unresolved state and escalate.
- Model provider timeout: fail visibly and allow safe retry or manual review.
- Authorization failure: verify the authenticated identity and server-side access policy.
- Data retention or deletion issue: preserve audit evidence and escalate to the privacy owner.

Never share credentials, patient records, prescription images, raw prompts, or unredacted logs when requesting help.
