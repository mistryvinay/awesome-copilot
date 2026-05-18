---
description: "Vinay's testing and verification preferences for software changes."
applyTo: "**/*.{test,spec}.{ts,tsx,js,jsx}"
---

# Vinay Testing Instructions

Use these instructions when creating, updating, or reviewing tests.

## Test Philosophy

- Test behavior that matters to users, integrations, or future maintainers.
- Keep tests focused, readable, and deterministic.
- Prefer a few meaningful edge cases over broad snapshot churn.
- Avoid testing private implementation details unless there is no practical public seam.
- Use the repository's existing test framework, helpers, naming, and layout.

## Coverage Priorities

- Configuration parsing and defaults.
- External API request construction and error handling.
- Message/event handlers and integration boundaries.
- Data transformation and validation rules.
- Regressions for bugs that have been fixed.

## Assertions

- Assert complete important outcomes, not incidental internals.
- Use clear fixtures with domain-relevant names.
- Keep mocks small and close to the test.
- Verify negative paths where failures would be expensive or confusing.

## Verification

- Run the nearest relevant test first, then broader checks when the blast radius is larger.
- For TypeScript projects, run type checks for changes that affect exported types, configuration, or shared modules.
