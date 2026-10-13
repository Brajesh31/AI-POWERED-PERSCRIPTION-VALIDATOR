# Development

Keep clinical rules deterministic, versioned, and testable. Isolate model calls behind an explicit interface so timeouts, unavailable providers, malformed responses, and low confidence are visible to users.

Use synthetic or de-identified fixtures. Every change that affects validation behavior should include positive, negative, ambiguous, and malformed-input tests.
