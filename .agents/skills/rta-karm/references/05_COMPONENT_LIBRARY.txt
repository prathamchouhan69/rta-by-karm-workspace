# 05 — DESIGN SYSTEM AND COMPONENTS

**Role.** Design-systems engineer. You implement the brief's tokens and a component set that is unmistakably Ṛta-BY-KARM.

**Outcome.** `src/ui/` + `/gallery` with every component in every state, light and dark, normal and Calm motion, 100/150/200% text, and route-appropriate depth where it improves comprehension.

## Rules
- Components come from the brief's surface/depth grammar. Do not reuse retired components or restyle them.
- Use original 3D/depth and material response for meaningful visual surfaces; do not turn the shared component library into a repeated glass-card or animation effect. Keep forms and controls semantic, stable and directly operable.
- Any component that displays data must have a clear data-source contract and a DOM text equivalent. Components may not synthesize, total, round or locale-format financial values.
- Behaviour from accessible primitives (Radix or equivalent); looks are yours. Style `data-state`, not internals.
- Inputs use ≥16 px text (iOS zoom). Touch targets ≥44×44 pt even if the visual is smaller. Use `rem`; no fixed-height text containers.
- State is never colour alone (icon or text too). Focus ring ≥3:1.
- Money: `<Money>` accepts **only** `ZohoMoney`, renders verbatim in the tabular/mono face, right-aligned in tables, long-press copies exact text. Money-entry input accepts typed digits as text and never parses for display.
- Practice banner is a real component: clear, persistent, never decorative.

## Build order (each in gallery with tests before the next)
1. Primitives: Surface, route-aware Depth wrapper (uses prompt 04), Focus ring, VisuallyHidden, Sheet, Portal.
2. Actions: button family (primary, secondary, quiet, outline, destructive, icon, split, toggle, segmented, chip) with states default, hover (pointer only), pressed, focus-visible, disabled, loading, success, error. Press must visibly change depth/light, then settle.
3. Forms: text, number, money-entry (raw), password/passphrase, search, textarea, select/combobox, date/range, checkbox, radio, switch, stepper, quantity, PIN, file attach, field wrapper with label/hint/error.
4. Feedback: toast, banner (info/success/warning/danger), skeleton, empty/error/offline/practice states, status pill (Draft, Sent, Overdue, Paid, Void…), progress, tooltip, popover, loader family.
5. Layers & navigation: modal, bottom sheet (snap points, swipe down), action sheet, menus, command palette, tabs, segmented control, accordion, wizard.
6. Data: route-specific visual surfaces, card, stat card (value is a Zoho string), list row (swipe actions), virtualised data table (5,000 rows; sticky header + first column), key-value list, timeline, avatar, chip. Every visual state is paired with complete labels/values in DOM; a chart/graphic is never the only data view.
7. Type roles: display, heading 1–4, body, label, caption, figures.

## Verify
Vitest + Testing Library for behaviour; Playwright WebKit for `/gallery`: screenshots of every section, axe zero serious/critical, tab-through shows visible focus, every control ≥44 px by `getBoundingClientRect`, no horizontal scroll at 375/402/440, pressed vs released screenshots differ. `scan:money` passes on `ui/`.

## Done means
- [ ] Every component in every state in the gallery; evidence paths saved.
- [ ] axe clean; contrast script clean; targets ≥44 pt.
- [ ] `<Money>` type-enforced; scan passes.
- [ ] Data-display components preserve source text exactly and expose all displayed data to assistive technology.
- [ ] Retired components still present only until prompt 13 removes them; no new code imports them.
