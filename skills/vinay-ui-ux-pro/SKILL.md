---
name: vinay-ui-ux-pro
description: "Use when designing, implementing, or reviewing user interfaces, product flows, frontend layouts, accessibility, responsive behavior, visual polish, or design-system alignment."
---

# Vinay UI UX Pro

Use this skill as a senior product designer and frontend UX engineer. This skill includes a searchable UI/UX reference set with styles, color palettes, typography pairings, product patterns, charts, web interface rules, React performance notes, and design reasoning guidance.

## When To Use

- Designing or improving screens, flows, dashboards, forms, tools, or landing pages.
- Reviewing UI for usability, hierarchy, accessibility, responsiveness, and visual quality.
- Translating rough product intent into polished frontend implementation.
- Working with React, TypeScript, Vite, Tailwind, component libraries, or design systems.

## Product Principles

- Build the actual usable experience first.
- Prefer clear workflows, fast scanning, and predictable controls.
- Match density and tone to the product context.
- Operational tools should feel quiet, efficient, and trustworthy.
- Consumer or creative experiences can be more expressive when the domain calls for it.
- Use existing design-system components before creating bespoke UI.
- Remove decorative UI that does not help the user understand, decide, or act.

## Searchable Design System Assets

When the user asks for design, redesign, implementation, or UI review work, start by generating design-system recommendations from this skill's bundled data when Python is available.

From this skill's base directory, run:

```bash
python3 scripts/search.py "<product type> <industry> <style keywords>" --design-system -p "<Project Name>"
```

Use detailed searches when useful:

```bash
python3 scripts/search.py "<keyword>" --domain ux
python3 scripts/search.py "<keyword>" --domain color
python3 scripts/search.py "<keyword>" --domain typography
python3 scripts/search.py "<keyword>" --domain chart
python3 scripts/search.py "<keyword>" --stack react
```

Available domains include `product`, `style`, `typography`, `color`, `landing`, `chart`, `ux`, `react`, `web`, and `prompt`.

Available stacks include `html-tailwind`, `react`, `nextjs`, `vue`, `svelte`, `swiftui`, `react-native`, `flutter`, `shadcn`, and `jetpack-compose`.

If Python is unavailable, use the guidance in this `SKILL.md` directly and continue without blocking the user.

## UI Implementation Guidance

- Inspect existing components, styles, tokens, and layout conventions before editing.
- Use stable layout constraints: grid tracks, flex rules, aspect ratios, min/max widths, and explicit control sizes.
- Keep text readable and make sure it fits its container at mobile and desktop sizes.
- Avoid nested cards and ornamental wrapper sections.
- Use icons for familiar actions where they improve scanning.
- Prefer semantic HTML, accessible names, visible focus states, labels, and useful validation states.
- Check responsive behavior across small mobile, tablet, desktop, and wide desktop viewports when possible.
- Preserve performance by avoiding unnecessary animation, layout thrash, and heavy visual effects.
- Use SVG icons from a consistent icon set such as Lucide, Heroicons, or the existing project icon system instead of emoji icons.
- Add pointer and hover feedback to interactive cards and controls.
- Keep hover states stable; avoid scale transforms that shift layout.
- Verify light and dark mode contrast when the project supports themes.
- Account for fixed navigation height so content is not hidden underneath it.

## Review Checklist

Look for:

- Confusing information hierarchy.
- Missing primary action or unclear next step.
- Layout overflow, overlap, clipping, or unstable resizing.
- Inconsistent spacing, alignment, typography, or control styling.
- Poor keyboard flow, focus visibility, labels, contrast, or touch target sizing.
- Empty, loading, error, and success states that do not help the user recover.
- Copy that is too long, too vague, or placed where it slows the workflow.
- Incorrect brand icons, inconsistent icon sizing, or icon sets mixed without intent.
- Hover effects that cause layout shift.
- Light-mode glass effects or muted text with insufficient contrast.

## Output

When reviewing, report the highest-impact issues first. Include the affected screen, component, or file when known. Suggest concrete fixes and verify visually after changes when tools are available.

## Pre-Delivery Checklist

- No emoji used as production UI icons.
- Icons are from a consistent icon system and sized consistently.
- Interactive elements have clear hover, active, disabled, and focus states.
- Text contrast is readable in every supported theme.
- Responsive behavior works at 375px, 768px, 1024px, and 1440px when practical.
- No horizontal mobile scroll unless it is an intentional data-table pattern.
- Forms have labels, validation states, and recovery guidance.
- Motion respects reduced-motion preferences.
