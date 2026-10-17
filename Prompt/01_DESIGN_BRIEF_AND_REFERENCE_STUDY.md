# 01 — VISUAL BRIEF FROM THE REFERENCE VIDEOS

**Role.** Art director and motion designer. You study references for craft and produce one original direction. You do not trace them.

**Outcome.** `reports/design/` containing the brief, tokens draft, motion grammar, route/data visual map and a reference-study log, before any screen is built.

**Inputs.** All seven owner videos (`2026-10-16 12-36-51.mp4` … `13-19-18.mp4`), `VIDEO_STUDY.md`, `imp.txt` (historical demo code, reference only), the current app and the current FORMWORK design authority.

## Steps
1. **Inspect the actual references.** Confirm all seven videos and `imp.txt` exist. Record duration, dimensions, frame rate and audio availability. Inspect the full videos when tooling permits; otherwise extract representative frames and short motion bursts, record the exact sample count and state that the inspection was not frame-by-frame. Use the existing contact sheets/burst sheets when they are evidence, not as a substitute for disclosing limits.
2. **Per video, log observations** (not opinions): what moves, what remains still, the user action that causes change, estimated timing, depth cues, materials, type hierarchy, density, colour roles and motion settling. Mark estimates and unknowns explicitly; do not infer narration when audio was not transcribed.
3. **Study `imp.txt` as untrusted historical demo code.** Identify its reusable craft ideas (linked chart/legend, period switching, restrained settling, material response, distinct loading states) and its unsafe or unsuitable patterns (fabricated values, simulated multipliers, money arithmetic, rounding, locale formatting, canvas-only labels, framework assumptions and copied component code). Do not paste, install, or ship its component or dependencies without independently verifying need, licence, compatibility and data-safety.
4. **Translate principles, not source designs.** Confirm or reject each starter principle with evidence. Keep the original FORMWORK casting-yard direction. Create new geometry, composition, materials, palette use and transitions; never reproduce a screenshot, card arrangement, object, text or signature animation.
5. **Map the complete product.** Create `ROUTE_DATA_VISUAL_MAP.md`: every route and meaningful data field/state—including agent/chat messages, tool status, notifications, search results and records—→ authoritative source → visual encoding → exact DOM text/table equivalent → loading/empty/error/offline/practice behaviour. Identify unavailable fields rather than inventing them. Every charted record/value must be traceable to the data source. Select at least 50 owner-supplied nature/math/structure/chart cues for integration into their related tasks, not a single Atlas sheet.
6. **Write `DESIGN_BRIEF.md` (one coherent direction).** Include audience and jobs; five personality words; palette roles; type system; surface/depth grammar; per-route and per-chart visual treatment; data-to-shape rules; motion tokens; responsive rules (375/402/440 px and desktop ≥1024); renderer/performance budgets; accessibility and no-WebGL fallbacks; explicit originality boundaries.
7. **Ensure every route has visual depth.** Apply route-specific, purposeful 3D or 2.5D visual treatment to the shell and to every meaningful visual/data surface, including chat/agent and loading/status states. Data visualisations must encode the actual Zoho records/fields, with stable labels and relationships. Keep messages, labels, values, legends, tooltips and accessible equivalents as selectable DOM text; use WebGL/Canvas only for geometry and decoration. A static still must preserve identical information.
8. **Draft tokens** (`design-tokens.json`): colour roles (light and dark), type scale, spacing (4/8 grid), radii, elevation/depth (z0–z5), blur, border, motion durations/easings/springs, breakpoints and performance tiers. Generate CSS variables with a script.
9. **Contrast script** (`scripts/contrast.mjs`): every text/UI pair in both themes, WCAG 2.2 AA (4.5:1 text, 3:1 large text and UI parts). Output `reports/design/contrast-report.md`. Include `#4F669C` on every surface it appears; on dark surfaces use a lighter tint for text if the ratio fails.

## Starter principles (from the videos — verify, then adapt)
- **Material answers touch.** Surfaces lean, settle or open in response to the point of contact and then rest. On touch devices use touch position and press, not hover.
- **Physical settling.** Motion ends with a short, damped spring, never a hard stop and never a long wobble.
- **Camera restraint.** Depth comes from layers and small bounded parallax (≤6°), not from swinging cameras.
- **Layered typography.** One expressive display moment per screen (serif/italic contrast on warm paper was the editorial cue); the rest quiet and exact.
- **Linked highlighting.** Legend row ↔ chart mark highlight each other; the chart explains itself.
- **Segmented time control.** Period switch (week/month/quarter/year) morphs the data view instead of replacing it.
- **Texture as data language.** Dither/stipple can express part-to-whole or progress; it must never reduce legibility.
- **Loaders have character.** A loader family with distinct motion per state (waiting, syncing, sending, failed) beats one generic spinner.
- **Rearrangeable density.** A dashboard the user can reorder is a task feature; persist the order.
- **Material shifts, not just colour.** A hover/press state can change texture or light, not only hue.
- **Distinct visual treatment per route.** Shared tokens and renderer create coherence; each route's geometry and motion communicate its own job instead of repeating one animation.
- **Data maps to form.** Spatial depth, size, position and movement may encode only a documented source field or interaction state. Never use an ornamental object to imply unprovided business facts.

## Hard cautions found in the reference code
- Reference widgets use count-up animation, rounding, locale formatting and simulated data. None of those patterns may transform Zoho money or be copied into production. Animate counts only when motion helps and reduced motion is respected.
- Reference charts use fabricated values and demo multipliers. Ṛta-BY-KARM uses source-backed fields or an honest empty/practice state; never derive money, totals, percentages or period multipliers in the interface.
- Canvas-painted text (pixel-fill headline) is not selectable. Use only for decoration with real DOM text present.
- Third-party components credit their authors. Do not ship them as-is.
- Shadcn/Tailwind/React/Motion code in `imp.txt` is not assumed compatible with the current stack. Reuse ideas only after checking the existing codebase and its conventions.

## Done means
- [ ] All seven videos and `imp.txt` inspected; exact coverage and limits recorded.
- [ ] `DESIGN_BRIEF.md`, `ROUTE_DATA_VISUAL_MAP.md`, `design-tokens.json`, `MOTION_GRAMMAR.md`, `contrast-report.md` exist.
- [ ] Originality check completed for all eight reference ideas.
- [ ] `STATUS.md` updated with evidence.
