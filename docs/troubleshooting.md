# 🧯 Troubleshooting

## Current status

There is no executable application to troubleshoot yet. The repository currently contains project documentation only.

## Future issue report format

When code is introduced, report:

- Exact command and affected component.
- Operating system and runtime versions.
- Sanitized configuration.
- Expected behavior and actual behavior.
- Minimal reproduction using synthetic values.
- Relevant redacted logs and correlation identifier.

## Common future failure categories

| Problem | Safe diagnostic direction |
|---|---|
| Unsupported upload | Check documented format and size limits |
| Ambiguous extraction | Request human confirmation; never guess |
| Missing prescription field | Mark unresolved and require input |
| Reference source unavailable | Return an unable-to-assess state |
| Model provider timeout | Fail visibly and route to manual review |
| Authorization failure | Verify identity and server-side permissions |
| Data deletion issue | Preserve necessary audit evidence and escalate to the privacy owner |

Never share credentials, patient records, prescription images, raw prompts, or unredacted logs in public support channels.
