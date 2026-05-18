---
description: "Vinay's TypeScript, Vite, and frontend application engineering preferences."
applyTo: "**/*.{ts,tsx,js,jsx,mts,cts}"
---

# Vinay TypeScript And Vite Instructions

Use these instructions when working in TypeScript, JavaScript, Vite, React-style frontend code, browser integrations, or small web application modules.

## TypeScript

- Prefer strict, explicit TypeScript over broad `any` or assertion-heavy code.
- Model domain data with named types or interfaces near the boundary where they are used.
- Keep functions small, composable, and easy to test.
- Prefer pure functions for transformation, parsing, formatting, and request construction.
- Use discriminated unions for state or message variants when they make invalid states harder to express.
- Avoid ambient globals unless the platform integration requires them.
- Keep side effects at the edges: bootstrap, transport, storage, DOM integration, and external APIs.
- Preserve useful error context when wrapping failures.

## Vite And Browser Apps

- Use Vite conventions and existing project scripts before adding custom tooling.
- Keep environment reads centralized and validated.
- Do not leak server-side secrets into browser bundles.
- Prefer relative asset-safe configuration when apps may be embedded, hosted under subpaths, or loaded in webviews.
- Keep development proxy behavior explicit and documented when backend calls are involved.

## Dependencies

- Prefer standard platform APIs and existing project dependencies.
- Add new packages only when they remove meaningful complexity or provide a proven domain capability.
- Check package fit, maintenance, bundle impact, and security before introducing it.

## Testing

- Use Vitest for unit tests when present.
- Test observable behavior rather than implementation details.
- Cover edge cases around parsing, configuration, external messages, request payloads, and error paths.
