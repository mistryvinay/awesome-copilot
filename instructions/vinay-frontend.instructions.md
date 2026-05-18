---
description: "Vinay's frontend UI, UX, accessibility, and interaction design preferences."
applyTo: "**/*.{tsx,jsx,html,css,scss,sass,less}"
---

# Vinay Frontend Instructions

Use these instructions when designing, implementing, or reviewing user interfaces.

## Product And UX

- Build the actual usable workflow first, not a decorative landing page.
- Match the UI density to the product domain. Operational tools should be calm, scannable, and efficient.
- Make common actions easy to find, fast to repeat, and hard to misuse.
- Use clear hierarchy, consistent spacing, and predictable navigation.
- Prefer direct manipulation and familiar controls over custom interaction patterns.
- Do not add in-app explanatory text about obvious UI behavior or implementation details.

## Visual Design

- Use existing design-system components and tokens where available.
- Keep cards for repeated items, modals, and genuinely framed tools; avoid card-inside-card layouts.
- Avoid decorative gradients, blobs, and ornamental backgrounds unless they serve the product.
- Use icons for familiar actions when an icon improves scan speed.
- Keep border radii restrained unless the existing design system says otherwise.
- Ensure text fits its container on mobile and desktop.
- Avoid layouts where text, controls, or panels overlap at common breakpoints.

## Accessibility

- Use semantic HTML and accessible names for interactive controls.
- Preserve keyboard navigation, visible focus states, and logical tab order.
- Maintain readable contrast.
- Respect reduced-motion preferences for animation.
- Use form labels, validation messaging, and error states that help users recover.

## Responsive Implementation

- Define stable layout constraints with grid, flex, aspect-ratio, min/max sizes, and sensible breakpoints.
- Test small mobile, tablet, desktop, and wide desktop viewports for meaningful UI changes.
- Keep touch targets usable on mobile.
- Avoid viewport-scaled font sizing.
