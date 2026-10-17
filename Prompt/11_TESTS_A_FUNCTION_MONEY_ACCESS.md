# 11 — TESTS A: FUNCTION, MONEY, ACCESSIBILITY, VISUAL, PERFORMANCE

**Role.** QA engineer who reports facts. A fake PASS is worse than an honest FAIL.

## Steps
1. **`reports/TEST_PLAN.md`:** ≥150 rows (ID, area, what, how, expected, file) covering every route, component state, document kind, relevant chart type, lock, offline queue, task-contextual nature integrations, self-test, settings, theme, Calm mode, no-WebGL.
2. **Unit/component coverage** from the tool (targets: 90% proxy, shared, money, motion maths, offline queue; 80% UI). Save the report.
3. **E2E on WebKit iPhone 16 Pro** for every route: no console errors, no unexpected failed requests, no horizontal scroll, top row below safe inset, nav present, screenshot saved. Journeys J1–J12 (first run/lock; quote → order → invoice; challan + invoice + PDF; partial payment; credit note; offline drafts; search; agent command; every supported chart tooltip; context-linked nature explanation returns to its task; theme/Calm/200% text; sign out clears cache) each run three times in a row; all three must pass. Assert no standalone all-items Atlas/gallery page is exposed.
4. **Accounting golden tests A1–A16** against the mock (golden invoice `₹64,944.84`; trailing zeros; tax lines; GST rates; decimals; discounts; credit/payments; ageing text; **no total while editing**; outgoing bodies contain no computed fields; invoice numbers verbatim; FY boundary; scan; `displayGeometry` geometry-only; CSV equals Zoho text). One row per test with evidence. These prove the app does not alter numbers; they cannot prove the mock equals real Zoho.
5. **Accessibility:** axe on every route in light, dark, Calm and 200% text; keyboard-only run of core journeys; focus order and visible focus; 44 pt targets; colour never alone; reduced motion/transparency; VoiceOver checklist `tests/a11y/VOICEOVER_CHECKLIST.md` (`NOT RUN` until a person runs it).
6. **Performance:** Lighthouse mobile (perf/a11y/best-practices/SEO) on key routes; bundle budgets; WebGL tier behaviour; frame time while scrolling (label emulated).
7. **Visual regression and data parity:** baselines for shell, every route and state, light/dark, Calm/reduced-motion, no-WebGL, three phone widths + desktop. For every chart/data visual, compare every plotted item, label, tooltip, table and exported value with its source record/text; test the exact product name in customer-facing UI and metadata.
8. **Fix failures:** log each in `BUGS.md` (ID, route, steps, expected, actual, evidence). Never weaken or delete a test to pass.
9. **Reports:** function, accounting, accessibility, performance — each ends with counts (total/passed/failed/not run).

## Done means
- [ ] All four reports exist with raw evidence under `reports/raw/`.
- [ ] Route/data visual coverage and exact brand-name checks are included with evidence.
- [ ] Journeys pass 3/3 or failures are logged.
- [ ] `STATUS.md` updated.
