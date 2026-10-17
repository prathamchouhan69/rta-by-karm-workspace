# 07 — MONEY DASHBOARD AND CHARTS

**Role.** Data-visualisation designer-engineer. Clarity first; the display of Zoho's numbers must be trustworthy.

**Outcome.** A new Money page and chart system. Migrate in small batches: (a) Money page, (b) chart engines + frame, (c) chart gallery families.

Every Money/chart surface must have original spatial depth and purposeful motion
that helps explain the real data, inspired by the craft observations in the
videos but never copying their compositions. Use 3D forms only where the data
mapping remains truthful and readable; give each surface a route-appropriate
visual identity instead of repeating one effect. Always expose every value and
label as exact, selectable DOM text with a complete accessible table.

## Data law for charts
- Source of every figure: a Zoho-calculated field or Zoho report. If none exists, show the list of Zoho values plus **Open in Zoho Books**. Never sum to invent totals.
- **Shape vs text:** geometry (bar height, arc angle) may be computed only inside the allow-listed `displayGeometry.ts`, which returns numbers only and can never produce text. Every label, axis value and tooltip is Zoho's string or non-money text (dates, names, counts). Axis ticks use only values present in the data; never invent round numbers.
- **3D data encoding:** depth, height, area, position, grouping and animation may encode only documented source fields/relationships. `displayGeometry.ts` may derive geometry only; it must not calculate displayed money, percentages, totals, rankings or text. If exact semantics cannot be implemented without prohibited arithmetic, show source rows instead.
- No count-up on money. Counts may animate briefly (respecting reduced motion).
- Reference demos fake data. You never do. No data → honest empty or practice state.

## Money page content (each card: skeleton, error+retry, "as of" when offline, source note)
1. Outstanding receivables per customer (Zoho's own figures, Zoho order, top 8 + see all)
2. Invoices needing attention (overdue first)
3. GST (Zoho tax report, else tile "GST lives in Zoho Books")
4. Revenue over time (one point per Zoho invoice; no monthly sums)
5. Cash and bank balances (Zoho bank accounts, as text)
6. Customer concentration (Zoho-provided figures as blocks)
7. Material mix (items with Zoho line amounts)
8. Transport/trips if Zoho service items exist
9. Counts: invoices by status, drafts waiting, offline queue size
Filters (period, customer, status) are sent to Zoho; the app never filters then re-adds money. Allow the user to **reorder cards** and persist the order locally (a task feature, not decoration).

## Chart system
- Engines built once, presets declared per chart. Inventory the chart types genuinely relevant to Karm Enterprises' work and supported by available Zoho fields/reports: comparisons, per-record trends, status/count distributions, due-date calendars, verified document flows/relationships, inventory/material views, and trip/transport views when those records exist. Build every relevant supported type; do not build unrelated types merely to fill a gallery or satisfy a generic taxonomy.
- Rendering: route-aware shared WebGL renderer for charts whose depth improves comprehension, with SVG/Canvas 2D still equivalents and cached off-screen views; ≤3 animated charts at once. Use 2.5D/SVG for charts where 3D distorts or hides the data. Record Tier A (true 3D), Tier B (2.5D) or static and the reason in `CHART_MATRIX.md`. Use d3 modules for geometry only.
- Original visual language from the brief. A texture/dither treatment for part-to-whole is allowed if every segment remains readable and labelled.
- Interaction: linked legend ↔ mark highlight; tap/focus shows a tooltip with Zoho text; period switch morphs; Calm mode = static, instant.
- Every `<ChartFrame>`: title, one-line plain description, a real accessible `<table>` of all source text values, and **Export CSV** that writes the exact source text. Do not hide essential content from assistive technology. Meaning never by colour alone (shape/pattern/label).
- `CHART_MATRIX.md` is the exhaustive business-relevant chart inventory: for each candidate type record its user question, route, exact Zoho source/fields, data availability, visual encoding, accessible table, and status (`SUPPORTED`, `NOT AVAILABLE FROM ZOHO`, or `NOT MEANINGFUL`). `/charts` contains only supported, meaningful charts using genuine Zoho/mock-contract data. Do not fabricate datasets for maps, statistical plots, or any other chart family. If a required field/report is unavailable, show a truthful unavailable state and **Open in Zoho Books** where applicable.
- Cover all useful chart forms that answer real business questions, including multiple forms when each reveals a distinct fact. Do not force every possible chart type onto one page.

## Verify
Unit: `displayGeometry` output is geometry-only and string-free; every supported preset builds with mock, empty, 1-point and 5,000-point data. Scan: zero violations. Playwright: every supported chart renders, accessible table equals the mock's source text, tooltip text equals source text, no console errors; golden invoice shows `₹64,944.84`; scroll `/charts` and record frame time (label emulated). Verify each chart's plotted records and geometry against its documented source mapping; axe clean; no label overlap at 402 wide; Calm and no-WebGL views preserve the same data.

## Done means
- [ ] Money page migrated; `DASHBOARD_FIGURES.md` lists each figure's Zoho source.
- [ ] `/charts` contains all and only supported, business-relevant chart types; every candidate is accounted for in `CHART_MATRIX.md`.
- [ ] Every Money/chart visual maps to documented source data with a complete accessible equivalent.
- [ ] Hidden table + CSV on every chart; scan passes.
- [ ] `STATUS.md` updated per batch with evidence.
