# 02 — FOUNDATION AUDIT AND GUARDRAILS

**Role.** Staff engineer. The app already exists. Audit first, build only what is missing.

**Outcome.** `INVENTORY.md` (routes, journeys, data provenance, working tree) and a verified guardrail layer that makes the redesign safe.

## Steps
1. `git status`, `git log -5`, `git stash list`. Record uncommitted files in `INVENTORY.md` and **do not touch them**. Create branch `redesign/rta-v2`.
2. **Route inventory.** Table: route, purpose, data sources (Zoho endpoint / local / static), auth required, states handled (loading/empty/error/permission/offline), owner of the file. Expected routes: `/today /money /documents /documents/:type /documents/:type/:id /customers /vendors /charts /atlas /agent /settings /gallery /selftest /lock /motion-lab` — mark which exist.
3. **Journey inventory.** Record the real workflows to preserve: first-run passphrase + lock, quotation → sales order → invoice, challan + invoice + Zoho PDF, partial payment, credit note, offline drafts, search, agent commands, charts/tooltips, task-contextual visual explanations, theme/Calm/text size, sign out. Do not assume an all-items Atlas browse page is required.
4. **Money-law guard.** Confirm `ZohoMoney` branded string type, `formatIndianGrouping` (string slicing only), and the zero-math scan (ESLint rule + `scripts/zero-math-scan.mjs`) exist and pass. If missing, build them: reject `+ - * / % ** parseFloat parseInt Number() unary+ BigInt .toFixed .toPrecision Math.round|floor|ceil|trunc Intl.NumberFormat toLocaleString` and `reduce`/loops on money-named operands. Allow-list only `groupDigits.ts` and `charts/displayGeometry.ts` (which may never return strings). Prove with ≥25 bad and ≥15 good fixtures.
5. **Exact-name migration (release blocking).** In the actual app source, change every customer-facing app-name string to exactly `Ṛta-BY-KARM`. Inspect and update the web document/browser title, visible shell/wordmark, PWA manifest `name` and `short_name`, iOS/apple title and installed label metadata, splash/loading/lock/sign-in/onboarding, settings/About, notifications, and current install/help guides. Search source and built output for alternate app-name spellings and abbreviations; every user-facing app-name occurrence must use the exact Unicode `Ṛ` (U+1E5A), hyphenation and casing. Verify the glyph in browser and install surfaces. Leave internal package names, API identifiers, database keys and historical provenance unchanged unless a safe migration is specifically needed. Save search results and evidence. If the app source checkout is unavailable, record this item `BLOCKED(reason: app source checkout unavailable)`; never mark the rename done.
6. **Glyph check.** Confirm the selected fonts and every relevant browser/iOS rendering path show `Ṛ` (U+1E5A) correctly, including PWA title and installed label. If a font lacks it, change the font, not the product name.
7. **Visual-data boundary.** Verify every route/data surface has a mapping in `ROUTE_DATA_VISUAL_MAP.md`, a source-backed visual encoding, and a complete DOM equivalent. Confirm rendering logic cannot introduce synthetic data or mutate displayed source values.
8. **Quality gates.** TypeScript strict, ESLint with a11y rules, Vitest, Playwright WebKit project `iphone-16-pro` (402×874 @3x, touch, en-IN, Asia/Kolkata), axe. Scripts: `dev build typecheck lint test scan:money test:e2e verify`.
9. **Baseline.** Run `verify` on the untouched tree and save results to `reports/raw/baseline-<timestamp>.txt`. Any pre-existing failure goes into `BUGS.md` as pre-existing so it is not blamed on the redesign.
10. **Screenshot baseline.** Capture every current route (light/dark) to `reports/baseline-screens/`. They are evidence of what was retired, not a design source.

## Done means
- [ ] `INVENTORY.md` is complete and matches the repo; uncommitted work untouched.
- [ ] Zero-math scan and its self-test pass.
- [ ] Exact-name audit passes in customer-facing source and metadata; `Ṛ` renders.
- [ ] Every route/data surface is represented in the visual-data map.
- [ ] Baseline `verify` and screenshots saved.
- [ ] `STATUS.md` updated.
