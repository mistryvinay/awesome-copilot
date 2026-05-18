---
description: "Vinay's default engineering collaboration rules for Copilot and agentic coding sessions."
applyTo: "**"
---

# Vinay Engineering Instructions

Use these instructions as the default working agreement for software changes.

## Working Style

- Read the existing code before deciding on an approach.
- Prefer the repository's current patterns, naming, dependencies, and test style.
- Keep edits focused on the user's goal and avoid unrelated refactors.
- Make the smallest durable change that solves the real problem.
- Explain meaningful tradeoffs when there are multiple reasonable paths.
- Treat user changes in the working tree as intentional; do not revert them unless asked.
- Prefer clear, boring code over clever abstractions.
- Add abstractions only when they remove real duplication or match an established local pattern.
- Use precise names that describe domain intent rather than implementation mechanics.
- Leave comments only where they clarify non-obvious behavior or constraints.

## Delivery Standards

- Carry work through implementation, verification, and a concise summary.
- Run the most relevant tests or type checks before calling work complete.
- If tests cannot be run, state why and identify the remaining risk.
- Keep security, correctness, and maintainability above speed.
- Do not introduce new services, libraries, frameworks, or architecture patterns without a clear reason.
- Do not hide errors. Fail clearly, validate inputs, and preserve useful diagnostics.

## Repository Hygiene

- Keep generated files, lockfiles, and metadata changes out of scope unless required.
- Prefer existing package scripts over one-off commands.
- Update docs or project instructions when behavior, setup, or operating assumptions change.
- For pull requests and reviews, lead with bugs, risks, regressions, missing tests, and concrete file references.
