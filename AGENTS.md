# AI Desktop solution site UI constraints

These rules apply to every file under `design/solution-site/`.

## Product and audience

- Design for developers, solution providers, brand owners, and technical decision makers evaluating an embedded AI device platform.
- The page's primary job is to present a complete solution: problem, platform blueprint, capabilities, adoption paths, implementation evidence, and delivery boundaries.
- Preserve honest product boundaries. Do not add demo, purchase, video, or contact controls that do not perform the named action.
- Keep the AI-DeskTopBox platform and Smart Desktop Mimi reference product visibly distinct.
- Describe A133 as the reference implementation. Other SoCs are adaptation seams until their project validation is complete.

## Visual system

- Use the design tokens in `styles.css`; do not introduce isolated color, radius, shadow, or spacing values without extending the token system.
- Keep the desktop content width at 1200 px or less and base spacing on an 8 px rhythm.
- Body copy must remain at least 16 px on desktop and 15 px on narrow mobile. Avoid solving density problems by shrinking text.
- Maintain a deliberate type hierarchy. Limit each section to one primary heading and keep normal reading lines below roughly 80 characters.
- Use cards only when they express real grouping. Do not turn every paragraph or fact into an identical rounded card.
- Avoid decorative all-caps labels, arbitrary 01/02/03 numbering, repeated gradient washes, and entrance animations on every section.
- Use product imagery as the main visual identity. Keep surrounding decoration restrained.
- Never crop, redraw, recolor, retouch, regenerate, or recompress the provided product renders. Display them at their original aspect ratio and label concept imagery clearly.
- Use repository UI captures as implementation evidence. Preserve their aspect ratio, do not fabricate screen content, and keep mobile captures large enough to inspect individually.

## Layout and interaction

- Support desktop, tablet, and mobile deliberately; do not treat mobile as a scaled desktop.
- Keep interactive targets at least 44 by 44 CSS pixels on touch layouts.
- All interactive elements must work with keyboard focus and expose appropriate accessible names and ARIA state.
- Respect `prefers-reduced-motion`; use motion only to explain a user-triggered state change.
- Do not hide essential product information behind hover-only behavior.
- Keep controls and labels in plain Chinese understood by customers rather than internal implementation terminology.

## Verification gate

- Before completion, inspect real browser renders at approximately 1440 px, 900 px, and 390 px widths.
- Check the first screen, the architecture area, every tab state, the mobile menu, long Chinese text wrapping, focus visibility, and horizontal overflow.
- Run JavaScript syntax checks, HTML validation, and local resource-link checks.
- Report rendered observations separately from source-code checks. Never claim visual verification from code inspection alone.
