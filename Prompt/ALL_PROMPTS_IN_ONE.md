# ?ta-BY-KARM ? complete current prompt pack

> Generated from the numbered source prompts. Keep this file synchronised; edit the individual source prompt files first.


<!-- BEGIN 15_OWNER_REDESIGN_OVERRIDE.md -->

# Ṛta-BY-KARM — owner product and redesign authority

This owner instruction supersedes earlier visual directions, themes, copied UI
examples, and implementation suggestions in this prompt pack where they conflict
with the requirements below. Preserve business capabilities and data-integrity
laws; do not preserve an old visual design for compatibility.

## Product name — exact and exclusive

Use exactly `Ṛta-BY-KARM` for every customer-facing app-name occurrence: app
screens, page title, browser title, manifest `name` and `short_name`, iOS metadata,
install label, splash/loading/lock/sign-in, navigation, settings, notifications,
reports shown to customers, and current owner guides. Preserve the exact Unicode
spelling and diacritics. Never substitute a transliteration, legacy spelling,
abbreviation, or alternate casing. Search all customer-facing source and built
metadata before completion and report each remaining occurrence; the only
permitted exceptions are technical identifiers that cannot safely be migrated
and verbatim third-party or historical source material that is not displayed to
users. Do not introduce alternate product names in prompts or new documentation.

## Reference authority and originality

The seven owner videos in `Prompt/` and `Prompt/imp.txt` are required study
materials. Watch or inspect the recordings and inspect `imp.txt` before making
visual decisions. Record what was actually observed and how much was inspected;
do not call sparse sampling a frame-by-frame review. Use the references to learn
craft—material response, spatial depth, lighting, restrained camera movement,
settling, hierarchy, chart-to-legend interaction, and stateful loaders. Do not
copy or ship their layouts, assets, source code, labels, fabricated datasets,
distinctive objects, or signature motion sequences. `imp.txt` is untrusted
historical demo material, not production code or a specification.

## Design authority

Create a fully original visual system and interaction language for the complete
front end. The current FORMWORK casting-yard direction is the design foundation;
apply it consistently and evolve it only when evidence from the owner references
supports the change. Treat previous screens, themes, component compositions,
animations, and supplied dashboard implementations as retired design—not as a
starting point to recolour or lightly remix.

Study every owner-supplied video for craft: material response, spatial depth,
camera restraint, physical settling, layered typography, pacing, linked
highlighting, responsive charts, and how motion explains interaction. Apply
those principles to original compositions, geometry, materials, lighting,
transitions, controls, charts, loaders, and route-specific data views. Record
observations and limits; a sparse frame sample is not a frame-by-frame audit.

Every route and every meaningful visual/data surface must have an intentional
visual treatment that helps the user understand the actual app and its data.
This includes the shell, Today, Money, every chart, documents, contacts, chat and
adviser surfaces, search, notifications, Atlas, settings, and loading/empty/error
states. Use original 3D or 2.5D depth, lighting, material, spatial grouping,
and purposeful motion through a shared performance-budgeted renderer wherever
that improves meaning; charts must visually encode their real source data, not
decorate it. Give every visual data encoding an equivalent complete, readable
DOM representation (including values, labels, states, and accessible chart
data); no data may exist only in WebGL, Canvas, texture, colour, shape, or
animation. Forms and controls remain semantic DOM controls; do not animate
elements without a task, data, or state purpose. Keep the business interface
first, never a marketing landing page. Motion must clarify data, hierarchy,
state, or interaction, and must never delay task completion or alter the
meaning of data.

Before implementation, define the audience and jobs, palette, type system,
surface/depth grammar, per-route visual mapping, motion tokens, responsive
rules, renderer and performance budgets, and accessible fallbacks. Give each
route a distinct, appropriate visual treatment rather than repeating one
effect everywhere. Integrate at least 50 distinct, selected owner-reference
cues into the tasks where they help; do not create a one-page Atlas/gallery of
all the cues. Prefer a calm, polished still pose over continuous motion.

## Preserve the product's invariants

- Zoho Books is the financial source of truth. Render its money text verbatim;
  never calculate, round, parse, or reformat money in the browser.
- Keep practice fixtures clearly labelled and separate from live data.
- Preserve authentication, authorization, proxy boundaries, offline handling,
  and existing business workflows while replacing their presentation.
- Use purposeful 3D/depth throughout visual and data surfaces; do not force
  controls or text into 3D. Keep a usable no-WebGL path, reduced-motion and
  Calm modes, keyboard/touch operation, and performance controls. Essential
  information and complete data remain available without motion or WebGL.
- Every chart and data graphic must map to real Zoho fields or explicitly
  labelled practice fixtures. Preserve row/record identity and exact source
  values; never fabricate, omit, aggregate, or imply a relationship the source
  does not provide. Computed chart geometry is permitted only under the
  allow-listed geometry boundary; it must not produce or transform display text.
- Do not invent missing records, owner assets, reference details, or test
  results.

## Delivery order

1. Inventory routes, user journeys, data provenance, every data surface, and
   the current working tree; protect existing uncommitted work.
2. Inspect all seven videos and `imp.txt`; produce an evidence-based visual and
   motion brief, recording what was and was not inspected. Do not copy them.
3. Establish and test design tokens, motion rules, shared 3D/depth renderer,
   fallback path, and a route-by-route data-to-visual map.
4. Redesign the shared shell and Today as the first complete vertical slice.
5. Migrate Money, documents, contacts, charts, Atlas, adviser, settings, and
   utility routes in small independently verified batches; account for every
   data field and state in the relevant screen or accessible equivalent.
6. Remove retired styles only after every route and visual data surface has
   migrated and been checked.
7. Search the source, UI, metadata, and customer-facing docs for the exact
   product name; verify it is always `Ṛta-BY-KARM`.
8. Verify mobile and desktop rendering, loading/empty/error/permission states,
   accessibility, reduced motion, no-WebGL fallback, performance, and the
   existing money scanner. Mark unavailable physical-device and live-service
   checks `NOT RUN`, not `PASS`.

Do not describe a partial route migration as a complete redesign. Update
`STATUS.md` after each finished slice with evidence and the precise next step.

<!-- END 15_OWNER_REDESIGN_OVERRIDE.md -->

<!-- BEGIN 00_RUNBOOK.md -->

# 00 — RUNBOOK (start here)

**Role.** You are a senior product designer-engineer redesigning an existing, working business app. You are not starting a prototype and you are not recolouring an old one.

**Outcome.** `Ṛta-BY-KARM`: an original, installable iPhone PWA for Karm Enterprises, built on the existing Zoho Books proxy, with every business workflow preserved, every data surface represented accurately, purposeful route-specific 3D/depth motion, honest evidence for every claim, and a `FINAL_REPORT.md`.

**Context.** Owner: Pratham Chouhan, proprietor of Karm Enterprises (Mandideep, Raisen, MP) — B2B supply of sand, stone dust, paver blocks, cement and pipes, plus transport. Main device: iPhone 16 Pro, one hand, often outdoors on building sites, often on weak networks. Zoho Books is the financial source of truth; the app is a window onto it.

## Workspace restore gate
Before app work, read the workspace-root `README.md`, `CONTINUE-HERE.md`, and
`STATUS.md`. In the 18 October 2026 workspace snapshot, the expected app checkout
is absent and the nested Git-metadata-only directory is not an app. If the actual
source, app-owned `README.md`/`STATUS.md`, and working tree are unavailable, stop
app implementation and runtime checks; record them `BLOCKED` or `NOT RUN` with
the reason. Use the workspace status only to understand the blocker, never as a
replacement for the app's own status. Historical build notes are not fresh test
evidence. Once the real checkout is restored, preserve its uncommitted work and
resume its first unfinished slice.

## Read order (mandatory)
1. `15_OWNER_REDESIGN_OVERRIDE.md` — owner authority. It wins every conflict.
2. This runbook.
3. The numbered prompt you are executing. Read it completely before touching code.
4. `archive/` holds historical prompts and data references. Use them only to verify existing data contracts; do not rebuild a standalone Atlas sheet or use archived visuals as design direction.

## Execution order (different from the old numbering)
| # | Prompt | Purpose |
|---|--------|---------|
| A | 00 + 15 | Inventory the current app and working tree. Protect uncommitted work. |
| B | 01 | Evidence-based visual brief from the owner's videos. No copying. |
| C | 05 (tokens part) + 04 | Design tokens, motion tokens, quality governor, fallbacks. |
| D | 06 | Shared shell + **Today** = first complete vertical slice. |
| E | 05 (components), 07, 08, 09, 03-UI parts | Migrate Money, Documents, Contacts, relevant Charts, contextual nature cues, Adviser, Settings and utility routes in **small verified batches**. |
| F | 10 | PWA, self-test, install. |
| G | 11, 12, 13 | Verification cycles and release. |
| H | 14 | Optional native wrapper (only if this machine is a Mac with Xcode). |
| — | 02, 03 | Run as **audits** of what exists. Build only what is missing. |

Remove retired styles only after every route has migrated and been checked (prompt 13).

## Core laws (apply to every prompt)
- **L1 Money.** Every money figure shown comes from Zoho as text and is rendered verbatim. The browser never adds, subtracts, parses, rounds or reformats money. Counts (7 invoices) are fine. The zero-math scan must pass.
- **L2 Evidence.** `PASS` only if you ran it and saw the output (raw output saved under `reports/raw/`). Otherwise `NOT RUN` with the reason. Never invent records, links, numbers, device results or owner assets. Never write "zero bugs" or "perfect".
- **L3 Original design.** Previous KARM screens, themes, compositions and animations are retired. Reference videos teach craft, not layout. No copied layouts, assets, code, text or signature animation sequences.
- **L4 Text is text.** All business data is selectable, readable DOM text. Canvas/WebGL never carries the only copy of information.
- **L5 Motion serves the task.** 3D only for orientation, material identity or interaction. Every motion has a reduced-motion form and a no-WebGL path. Nothing essential depends on motion.
- **L6 Secrets.** No keys, tokens, passwords or account numbers in code, logs, screenshots or reports.
- **L7 Brand files.** The owner's logo (and mascot, if supplied) are placed unchanged; hash recorded in `BRAND_ASSETS.md`. Swirl colour `#4F669C` is locked.
- **L8 Always runnable.** `npm run dev` and `npm run build` work at the end of every slice. Update `STATUS.md` after every slice with evidence and the precise next step.
- **L9 Preserve work.** Run `git status` first. Never discard uncommitted changes. Work on a branch; commit per slice.
- **L10 Language.** Customer-facing product name is exactly `Ṛta-BY-KARM` (browser title, install metadata, splash, sign-in, settings, guides). UK English. Asia/Kolkata. Indian digit grouping comes from Zoho strings.
- **L11 Product name.** Use exactly `Ṛta-BY-KARM` for every app-name occurrence in UI, metadata, install surfaces and current documentation. Do not abbreviate or transliterate it. Verify by searching the source and built output.
- **L12 Visual coverage.** Every route and meaningful data surface gets a deliberate visual treatment, with original 3D/depth/motion where it improves understanding. Every chart/data graphic must represent real source records faithfully and have a complete accessible DOM equivalent. Never use animation, colour or 3D as the only carrier of data.

## Autonomy
Nobody answers questions during the build. When unsure, choose the safest reversible option, log it in `DECISIONS.md` (choice, reason, alternatives) and continue. Spend at most five honest attempts on one problem, then log it in `BUGS.md` with the exact error and move on.

## STATUS.md format
Top table: `| Slice | Routes/files | State | Evidence path | Next step |`. States: `TODO`, `DOING`, `DONE`, `BLOCKED(reason)`, `SKIPPED(reason)`, `NOT RUN(reason)`. A partly migrated route is `DOING`, never `DONE`. Do not describe a partial migration as a complete redesign.

## Quality bar (reject your own work if it shows these tells)
Generic gradients; glass on every surface; identical rounded cards in a uniform grid; emoji or clip-art icons; one expressive effect repeated on every screen; count-up animation on money; decorative 3D without a data or interaction purpose; motion that shifts layout or delays work; pale grey on white or dim grey on dark; icon-only controls without labels; a marketing hero where a work screen should be.

## Done means
- [ ] Inventory file exists and matches the repo.
- [ ] Every route and data surface is mapped to its source, visual encoding and accessible text equivalent.
- [ ] All customer-facing app-name occurrences use exactly `Ṛta-BY-KARM`.
- [ ] Every route is `DONE`, `BLOCKED` or `SKIPPED` with evidence.
- [ ] `FINAL_REPORT.md` lists finished / partial / `NOT RUN` precisely, test report paths, open `BUGS.md` items and what the owner must do by hand.

<!-- END 00_RUNBOOK.md -->

<!-- BEGIN 01_DESIGN_BRIEF_AND_REFERENCE_STUDY.md -->

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

<!-- END 01_DESIGN_BRIEF_AND_REFERENCE_STUDY.md -->

<!-- BEGIN 02_FOUNDATION_AUDIT_AND_GUARDRAILS.md -->

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

<!-- END 02_FOUNDATION_AUDIT_AND_GUARDRAILS.md -->

<!-- BEGIN 03_ZOHO_PROXY_AND_MOCK_AUDIT.md -->

# 03 — ZOHO PROXY AND MOCK (AUDIT; UI-FACING CONTRACT)

**Role.** Backend engineer protecting the contract the new front end depends on. The proxy and mock exist; verify and extend only where the redesign needs it.

**Outcome.** A verified API contract (`reports/zoho/API_CONTRACT.md`) and practice-mode labelling the new UI can rely on.

## Non-negotiables
- The phone never holds Zoho secrets. The proxy holds refresh tokens (never logged, never in code). Access token cached in memory, one refresh at a time, retry once on 401, backoff on 429.
- Responses parsed losslessly (`lossless-json`); money fields stay exact text (`100.50` stays `100.50`). Prefer Zoho `*_formatted` fields.
- Writes accept only raw inputs (customer, items, typed quantity/rate/discount %, dates, notes, terms, chosen tax and place of supply). Bodies containing `total`, `sub_total`, `tax_total`, `balance`, `round_off` or tax amounts are rejected with 422.
- Every POST/PUT needs an `Idempotency-Key`; replays return the stored response; concurrent duplicates wait.
- Append-only audit log of the app's writes, labelled in the UI as "Ṛta-BY-KARM activity log" (not an accounting audit trail).
- Login: scrypt/argon2id passphrase, HttpOnly Secure SameSite=Strict cookie, lockout, CSRF, optional passkeys.
- Aggregates: only Zoho-calculated figures or Zoho reports. If Zoho has no endpoint, the UI shows "This lives in Zoho Books" with an **Open in Zoho Books** link. Never rebuild by arithmetic.

## Steps
1. Re-read Zoho Books API v3 docs if reachable; otherwise mark endpoints `unverified`.
2. Diff the existing routes against `ENDPOINT_MAP.md`: invoices, estimates, sales orders, delivery challans, credit notes, customer payments, retainer invoices, purchase orders, bills, vendor credits/payments, expenses, journals, contacts, items, taxes, PDF, search, news, agent, auth, audit, health.
3. **UI contract additions the redesign needs** (add only if absent): a `mode` field on every response envelope (`practice` | `live`) so every screen can label fixtures; `asOf` timestamp on cached/offline data; a stable error shape `{ ok:false, error:{ code, message, hint } }` the new error states can render; a `/health` that exposes no secrets or org details.
4. **Practice mode.** Mock data is clearly labelled, visually separate from live, and never mixed. The golden invoice `INV-KE-270031` shows `₹64,944.84` in practice mode.
5. Mock failure switches: 401, 429 (60 s), 5xx (30 s), 8 s latency, dropped connection, token store down — used by prompts 11–13.
6. `SETUP_ME.md` (six numbered steps to connect real Zoho, in plain words) and `LIVE_CHECKLIST.md` (20 owner-run checks). Keep practice mode on until all are ticked.
7. Contract tests: lossless parsing, idempotency storm (200 same key → 1 document), 422 on computed fields, redaction of tokens in logs.

## Done means
- [ ] `API_CONTRACT.md` matches the running proxy.
- [ ] Mode/asOf/error shape present and tested.
- [ ] Contract tests pass (or `NOT RUN` with reason). Nothing claims real-Zoho verification.
- [ ] `STATUS.md` updated.

<!-- END 03_ZOHO_PROXY_AND_MOCK_AUDIT.md -->

<!-- BEGIN 04_MOTION_AND_DEPTH_SYSTEM.md -->

# 04 — MOTION AND DEPTH SYSTEM

**Role.** Motion designer-engineer. You build a small, original motion language that makes interaction understandable and survives hot phones, Low Power Mode and Reduce Motion.

**Outcome.** `src/motion/` and the shared route-aware 3D/depth renderer, with tokens, springs, a quality governor, first-class fallbacks and a Motion Lab.

## Principles
- Motion explains: where something came from, what changed, what is pressable, what is waiting. If it explains nothing, delete it.
- Every route and meaningful visual/data surface uses purposeful depth or motion that supports its task; choose 3D, 2.5D or a carefully lit static treatment according to the performance tier. Do not force 3D onto text, controls or forms.
- Every chart's motion and geometry explain source-backed data or an explicit user action. The DOM remains the complete source of truth for labels, values, status and accessibility; visuals may never invent or obscure data.
- Budget before beauty: 120 Hz is available on iPhone 16 Pro, but the app must hold 60 on a warm phone.

## Steps
1. **Motion tokens** from `MOTION_GRAMMAR.md`: durations (instant 90 ms, quick 160, base 240, slow 420, scene 700), easings (named cubic-beziers), springs (press, settle, glide, lean, release) as stiffness/damping/mass data, depth scale z0–z5, perspective, max tilt (≤6° sensor, ≤12° pointer).
2. **Spring solver** (`spring.ts`): fixed inner step (1/240 s), semi-implicit Euler, never explodes, energy decays. One global rAF loop; no per-frame React state; `will-change` only while animating; ≤40 animating elements.
3. **Touch-lean primitive**: bounded tilt from touch/pointer position, settles on release; touch uses press point, not hover. Avoid motion that shifts layout or moves values. Optional gyro tilt only after an explicit tap on a labelled control (`DeviceOrientationEvent.requestPermission()`), low-pass filtered.
4. **Linked highlight primitive**: legend ↔ mark hover/focus/press sync with text-visible state.
5. **Loader family** (original): waiting, syncing with Zoho, sending queued items, failed/retry. Each state has a distinct but restrained form/motion grounded in the reference craft; each `role="status"` has text; static in reduced motion.
6. **Shared 3D renderer**: one fixed, route-aware WebGL2 context behind or beside content (`pointer-events:none` unless an accessible control explicitly owns the interaction), pixel ratio ≤2 × dynamic scale 0.6–1.0, pause on `document.hidden`, handle context loss/restore, pool objects. Provide route-specific data scenes/materials instead of a single generic effect. When a chart takes the renderer lease, release it cleanly from the shell. Never paint text or money into the canvas.
7. **Quality governor** (data-driven tiers ULTRA→STILL): EMA of frame time over 90 frames; step down on sustained slow frames, step up one tier after 12 s of good frames with a 20 s hold; drop to STILL on `Reduce Motion`, Calm mode, battery <15% unplugged, hidden page, or 30 fps frame cadence (Low Power Mode). Persist the best working tier.
8. **Fallbacks:** STILL tier = route-specific static lit composition (CSS/SVG/Canvas 2D); no-WebGL path is a first-class design, not an error screen; Reduce Transparency → opaque surfaces; Calm mode → no parallax, no particles, instant or short cross-fades, **all data and controls remain available**.
9. **Haptics:** feature-detected, best effort (iOS Safari lacks the Vibration API; the `input[switch]` tick trick may work on 17.4+). Mark real-device haptics `NOT RUN`.
10. **Motion Lab** (`/motion-lab`): switch tier, preview every token, loader and primitive; FPS, frame time, draw calls, heap if available; samples saved for the self-test.
11. **Route coverage.** Use `ROUTE_DATA_VISUAL_MAP.md` to verify the renderer/motion treatment on every route and meaningful data surface, including list, chart, loading, empty, error, offline and practice states. Avoid animating every item at once; semantic coverage does not mean continuous or simultaneous motion.

## Verify
- Unit: spring (stable, reaches target, energy decays), governor (fake frame times, no flip-flop), reduced-motion, tilt filter.
- Playwright WebKit: Motion Lab canvas non-blank after 2 s (or CSS path visible), screenshots at 0/5/10 s differ in normal mode and are identical in Calm mode, context-loss/restore survives, no console errors. Headless FPS is labelled "emulated, not representative".
- Verify each route has its intended original visual, exact DOM data parity, and a still/no-WebGL equivalent; screen recordings or snapshots must not claim unsupported live-device performance.
- Heap flat over ≥2 minutes (10 if time allows).

## Done means
- [ ] Tokens and primitives used by Today and the shell.
- [ ] Route-specific depth/motion and data mappings covered across all active routes.
- [ ] Every motion has a reduced form; no-WebGL path verified.
- [ ] Governor tests pass. Real-device smoothness is `NOT RUN` until the self-test runs on the phone.

<!-- END 04_MOTION_AND_DEPTH_SYSTEM.md -->

<!-- BEGIN 05_DESIGN_SYSTEM_AND_COMPONENTS.md -->

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

<!-- END 05_DESIGN_SYSTEM_AND_COMPONENTS.md -->

<!-- BEGIN 06_SHELL_AND_TODAY_FIRST_SLICE.md -->

# 06 — SHARED SHELL AND TODAY (FIRST COMPLETE VERTICAL SLICE)

**Role.** Lead product designer-engineer. This slice proves the whole direction. Do not start other routes until it is `DONE` with evidence.

**Outcome.** New shell + Today, fully real: data, states, accessibility, fallbacks, tests.

The shell and every Today data surface must express the FORMWORK visual language
through original, restrained 3D/depth and interaction motion. Give each data
group a purposeful encoding; keep all labels, values and actions as selectable
DOM content. Build from actual route sources and the route/data visual map—never
add decorative visuals that imply facts the source does not contain.

## Shell requirements (function preserved, presentation new)
- **Top row sits below the Dynamic Island safe inset** (iOS draws the clock/battery in the status bar; a web app cannot occupy the island). Order on **every** screen: **search on the left, sync-status in the middle, agent on the right** (plus notifications). All targets ≥44 pt. Log in `DECISIONS.md` why the row sits below the island.
- **Sync status** is a labelled live indicator: in sync with Zoho / waiting (offline queue) / problem / practice mode. Tap opens details (last sync, queue count). Status uses text plus shape, never colour alone.
- **Primary navigation:** Today, Money, Documents, More — thumb-reachable, text labels always visible, above the home bar (`env(safe-area-inset-bottom)`). Do not put a standalone Atlas or inspiration-gallery tab in the navigation; contextual visual explanations open from the relevant task and return to it.
- **Quick create:** New Invoice, Quote, Challan, Payment, Expense reachable in ≤2 taps from anywhere, each a text-labelled real button, also exposed as a plain list for VoiceOver. Choose the composition from the brief (the old starfish fan is retired).
- **Search sheet** and **Agent sheet** (command palette with deterministic commands such as "show unpaid invoices", "new invoice for <customer>", "what is overdue"; optional "Ask the advisor" via the proxy only, with an honest message if no provider is configured; no AI key in the app).
- **Chat/agent visual treatment:** give the conversation surface purposeful depth, clear message grouping, and restrained transitions for new messages, tool activity, waiting, success and errors. Messages, tool results and source references remain ordinary selectable DOM text; never paint chat content into a canvas or make meaning depend on animation.
- **Splash** (≤2.2 s, tap to skip, never blocks work) and **Lock** (logo, passkey, passphrase; blank content when hidden or locked so the app switcher shows only the brand; wipe sensitive memory on lock; lock after the configured idle or background time).
- **Theme:** Auto (Asia/Kolkata daylight with a soft crossfade), Light, Dark, System. Both pass the contrast script.
- **Mascot:** use the owner's mascot art unchanged if supplied; otherwise do not invent one unless the brief justifies it. If kept, states (idle, working, waiting, success, error, asleep) must also be conveyed by text/status, never by pose alone.
- **Logo:** the owner's file, unchanged, hash-verified. If missing: text wordmark "Ṛta-BY-KARM", log `MISSING_LOGO`, warn in Settings → About.
- **Layouts:** 402×874 design; support 375×667 and 440×956; portrait is the design, landscape must not break; `100dvh`; `viewport-fit=cover`; desktop ≥1024 gets a purpose-built layout, not a stretched phone.
- **Visual treatment:** one route-specific 3D/depth treatment establishes the yard; distinct data groups use calm, source-backed graphic encodings instead of a repeated animation. A no-WebGL/still pose preserves the same information and affordances.

## Today content (real, from Zoho/proxy; fixtures labelled)
1. **What needs me now:** overdue invoices (days overdue is a count; balance is Zoho text), due today, drafts to finish, offline-queue items.
2. **Quick actions** (the five creates).
3. **Sync card:** status, last sync, queue.
4. **Morning thought:** one item per day chosen by date (stable all day) from the existing `data/quotes.ts` (nature thoughts, Tesla items traced to his own writing or labelled "Tesla (paraphrased)", true nature facts). Preserve the existing bank; do not regenerate or invent quotes.
5. **News:** `/api/v1/news` (3 public RSS feeds, 30 min cache, title/link/source/time only), 5 items, "News is resting" on failure.
Design the screen as a **work surface first**: the first viewport answers "what should I do next?" Visual identity supports it; it never replaces it.

Map each displayed Today field to its source and visual encoding in
`ROUTE_DATA_VISUAL_MAP.md`. A Zoho value may appear in a chart only with its
exact text counterpart; the visual cannot change its meaning, precision, order
or status.

## States to design and test
Loading (skeletons shaped like the content), empty, error with retry, offline with "as of" time, permission denied, practice mode, locked, text size 200%, Calm mode, no-WebGL.

## Verify
Playwright WebKit iPhone 16 Pro screenshots for splash, Today (each state), top row (zoomed), nav, quick create, search, agent, lock, settings entry. Assertions: top row below the safe inset; search left of the status control, agent right; every control ≥44 px; logo hash matches; no overlap of floating elements with nav; morning thought changes by mocked date; locked state hides page text; axe zero serious/critical; no horizontal scroll at 375/402/440; scan passes. Repeat in dark, Calm and no-WebGL. Compare the accessible DOM values with the source data in every visual state.

## Done means
- [ ] Shell and Today live on real data paths; old shell unused by Today.
- [ ] All states designed and screenshotted; evidence under `reports/slices/today/`.
- [ ] Today data sources, visual encodings and DOM equivalents are documented and verified.
- [ ] Search and chat/agent states remain legible, accessible, and source-faithful in motion and Calm modes.
- [ ] Reduced motion, no-WebGL, keyboard operation verified.
- [ ] Physical-device checks marked `NOT RUN`.
- [ ] `STATUS.md`: Today `DONE`, next slice named precisely.

<!-- END 06_SHELL_AND_TODAY_FIRST_SLICE.md -->

<!-- BEGIN 07_MONEY_DASHBOARD_AND_CHARTS.md -->

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

<!-- END 07_MONEY_DASHBOARD_AND_CHARTS.md -->

<!-- BEGIN 08_DOCUMENTS_AND_ACCOUNTING.md -->

# 08 — DOCUMENTS, CONTACTS AND ACCOUNTING WORKFLOWS

**Role.** Product designer-engineer for high-stakes forms and lists. A site manager must complete an invoice one-handed in poor light without ever doubting a number.

**Outcome.** Redesigned Documents, Contacts and Offline flows. **Presentation changes; workflow, validation, idempotency and Zoho contracts do not.** Migrate in batches: (a) list + view, (b) editor, (c) actions + PDF, (d) offline queue UI, (e) contacts, (f) T&C and settings.

## Preserve exactly
- **Kinds:** Tax Invoice, Quotation, Sales Order, Delivery Challan, Credit Note, Customer Payment, Retainer Invoice, Purchase Order, Bill, Vendor Credit, Vendor Payment, Expense, Journal as full screens; reports Zoho's API lacks (balance sheet, P&L, trial balance, GST ledger, audit trail, statements) as honest "Lives in Zoho Books" tiles with **Open in Zoho Books**. Full + tile kinds ≥20 in `DOCUMENT_MATRIX.md`.
- **Editor (raw inputs only):** customer search, dates, terms, place of supply (Zoho list), reference, line items (item search; quantity and rate typed as text; rate prefilled from Zoho text; discount typed; tax **chosen** from Zoho's list), notes, T&C set. While editing, **no total is ever shown**; the exact sentence "Total will be calculated by Zoho Books" stays visible with **Save as draft in Zoho**. After Zoho replies, show the saved document with every figure as Zoho text.
- **Actions only as Zoho offers them** (send, mark sent, void, clone, convert estimate/sales order → invoice, record payment, apply credit, delete draft). Destructive actions need confirmation by typing the document number or long-press, in plain words. Every write carries an idempotency key.
- **PDF:** Zoho's own PDF via the proxy in a local pdf.js viewer; Web Share and Download. Never generate your own invoice PDF.
- **T&C sets:** ≥3 per kind, owner's own clauses word for word if found (quotation has eight numbered clauses); otherwise labelled drafts "DRAFT – owner to review. Not legal advice." No money amounts inside T&C text.
- **Offline queue:** raw inputs + key in IndexedDB; "Waiting for Zoho" state with no totals; ordered send; 4xx shows Zoho's message and keeps the item; 5xx retries with growing delays up to 8; cached documents readable offline with an "As of …" label.
- **Lists:** virtualised, instant search, status pills, pull to refresh, infinite scroll.
- **Contacts:** Zoho's outstanding receivable and unused credits as text; vendor equivalents.

## Design brief for this area
- Document view reads like a trustworthy statement: figures aligned, labels exact, status obvious, actions grouped by risk.
- Editor: one-handed reachability, sticky save area that survives the iOS keyboard (`visualViewport`), line-item entry optimised for repeated materials, large steppers, clear error placement.
- Visuals: give document kinds, lists, status, queue progress and record detail original FORMWORK depth/material treatments that make the real workflow and source state easier to understand. Do not turn every row into an animated object or repeat the same glass-folder treatment everywhere.
- Motion: list rows use restrained, purposeful depth; opening a document may use an original shared-element transition; every movement has a Calm/reduced-motion still equivalent; never animate, transform or render figures through a canvas.
- Data coverage: map every displayed document/contact/queue field to its Zoho or local source. Keep every record, exact figure string, status, label and error available as selectable DOM text; visual groupings may not imply unprovided relationships or hide items.
- States: loading, empty, error, permission, offline, practice, conflict.

## Verify (against the mock; say so in reports)
Journeys J2–J6 three times each; every `data-money` element equals the mock's raw text; outgoing bodies contain no computed fields; no total in the DOM while editing; trailing zeros survive; GST rates 0/5/12/18/28, zero-rated and exempt; decimals (0.001, 1234567.891); credit notes, partial payment, overpayment; financial-year boundary 31-03/01-04; offline: three drafts → exactly three documents. axe, 44 pt, keyboard and screenshots saved.

## Done means
- [ ] Every kind has its new screens and states; matrix complete.
- [ ] All preserved behaviours proven by tests or marked `NOT RUN`.
- [ ] Route-specific document visuals preserve complete record/source data in DOM and still/no-WebGL modes.
- [ ] No money maths; scan passes.
- [ ] `STATUS.md` updated per batch.

<!-- END 08_DOCUMENTS_AND_ACCOUNTING.md -->

<!-- BEGIN 09_NATURE_ATLAS.md -->

# 09 — TASK-INTEGRATED NATURE, MOTION AND DATA VISUALS

**Role.** Product visualisation designer-engineer. Translate selected natural,
mathematical and structural ideas into practical, original interactions across
Ṛta-BY-KARM.

**Outcome.** A working `NATURE_INTEGRATION_MAP.md` and at least 50 distinct,
purposeful reference cues integrated into the relevant app tasks—not a
standalone atlas page, inspiration gallery, or sheet of examples. Keep or
repurpose `/atlas` only as a contextual explainer reached from a relevant task;
it must never display every reference or item together.

## Owner intent

- The long reference list in the owner brief is an idea bank, not a checklist
  to exhaust. Select at least 50 distinct cues from it. More are allowed only
  when each has a real, useful task connection.
- Integrate selected cues into Today, navigation, document and contact
  workflows, search/chat, sync/offline states, charts, reporting and other
  applicable screens. Each cue must appear where the related task happens; do
  not gather them on a separate Atlas/gallery page.
- Build every chart and graph type that is genuinely relevant to Karm
  Enterprises' available Zoho Books data and workflows. Use Prompt 07's source
  and money rules. Do not build irrelevant chart types just to increase a
  chart count, and never create demo values to fill a chart.
- The FORMWORK casting-yard direction remains the visual foundation. References
  inform craft only; do not copy their layouts, objects, logos, code, colours,
  wording, or signature animation.

## Non-negotiable truth and access rules

- A natural or mathematical cue is a visual metaphor, not evidence about the
  business. Do not imply biological, financial, operational, customer, route,
  stock, or status facts that the app's source data does not establish.
- Every data mark must map to a named source field/record and have a complete,
  selectable DOM text equivalent. Provide accessible labels/tables for charts.
  No essential data may live only in a 3D scene, canvas, colour, motion, or
  shape.
- Zoho Books remains the source of financial truth. Display Zoho money strings
  verbatim; never calculate, round, parse, aggregate, estimate, or reformat
  money. Practice data must remain clearly labelled and separate from live.
- Use purposeful, route-specific 3D/depth and motion with a shared renderer.
  Motion should explain task state, data relationships or interaction. Keep a
  still/Calm/reduced-motion and no-WebGL equivalent. Never animate all objects
  at once or sacrifice readability, touch targets, battery, or performance.
- Do not invent missing Atlas records. Existing verified entries may be shown
  only when contextually relevant. Missing owner data remains missing and is
  recorded; it is not a blocker to using the owner-supplied reference cues.

## Minimum 50 task integrations

Create and complete this mapping before implementation. Adapt or reject an
example if the app has no suitable source or workflow; replace it with another
distinct cue from the owner's supplied list so at least 50 valid integrations
remain. “Integration” means a visible, tested treatment in the actual task
surface, not merely naming a motif in documentation.

| # | Reference cue | Task integration |
|---:|---|---|
| 1 | Honeycomb | Group the labelled quick-create actions into a compact, thumb-reachable cluster; each remains a real button. |
| 2 | Hexagonal tiling | Give source-backed material/item categories a distinct, orderly spatial grouping where the existing inventory data supports it. |
| 3 | Phyllotaxis | Use as a restrained arrangement principle for Today overview marks; positions must not encode priority unless the source order does. |
| 4 | Golden ratio | Inform the balance between Today's action list and contextual visual, never the size of a financial value. |
| 5 | Golden angle | Stagger independent decorative particles or entry timing; never use it to fabricate a chart distribution. |
| 6 | Logarithmic spiral | Shape a brief, skippable route transition or onboarding reveal; do not use as a data axis. |
| 7 | Fractal branching | Organise nested navigation/filter groups when those groups exist in the app's real routes or records. |
| 8 | Self-similarity | Keep repeated document/line-item groups visually coherent while preserving each record's text and identity. |
| 9 | Tree branching | Show real parent/child customer or document relationships only when the source explicitly provides them. |
| 10 | River meanders | Give a document's chronological activity/history a calm, readable path using source timestamps. |
| 11 | Catenary curves | Connect related documents in a relationship view when Zoho provides their identifiers. |
| 12 | Spider silk | Style the same verified relationship connectors as fine, low-noise lines; never imply an unrecorded link. |
| 13 | Orb webs | Offer a focused relationship view for a selected real record, not a global network of invented connections. |
| 14 | Web vibrations | Provide a small, accessible response when a form field or sync state changes; pair it with text feedback. |
| 15 | Ant colonies | Visualise the existing offline-send queue order; preserve FIFO and expose each queued item by name. |
| 16 | Honeybee waggle dance | Make the result of a user-triggered sync/send action clear through one restrained status motion plus text. |
| 17 | Fireflies | Mark newly received notifications with bounded emphasis and a readable timestamp/status. |
| 18 | Starling murmurations | Create a stateful loading transition for a collection only; never suggest the number of records before data arrives. |
| 19 | Beaver dams | Group unsent local drafts as a clearly labelled queue, with retry/removal actions and no computed totals. |
| 20 | Migratory corridors | Guide the user through due/overdue work ordered by Zoho's source dates/statuses. |
| 21 | Termite mounds | Use layered surfaces to distinguish primary actions, detail and secondary tools on dense screens. |
| 22 | Gecko feet | Keep relevant table/list headers anchored during scroll without obscuring rows or focus. |
| 23 | Lotus leaf | Give empty/offline states a calm surface and a clear next action; do not disguise an error as an empty result. |
| 24 | Morpho structural colour | Use a subtle material shift for focus/selection, with text, outline or shape as a non-colour cue. |
| 25 | Chameleon colour change | Make explicit theme changes feel continuous; never change a user's theme unexpectedly. |
| 26 | Octopus chromatophores | Distinguish practice/live mode through a persistent labelled treatment, not camouflage or colour alone. |
| 27 | Pinecone scales | Structure long document forms into progressive, labelled sections without hiding required fields. |
| 28 | Romanesco broccoli | Give genuinely nested categories a consistent repeating geometry; do not invent hierarchy. |
| 29 | Concentric circles | Focus a selected record or sync state; labels and values remain outside the canvas. |
| 30 | Triangular bracing | Use stable structural supports in the responsive shell, not as a claim about vehicle/load safety. |
| 31 | Hollow cross-sections | Present pipe item types only when those items exist in Zoho; use the product name/type as DOM text. |
| 32 | Layering | Separate document, action and status planes while keeping the full reading order in the DOM. |
| 33 | Tapering forms | Make a multi-step document workflow's current step visually evident without implying completion. |
| 34 | Interlocking shapes | Group a quotation/order/invoice sequence only when the linked source records confirm the relation. |
| 35 | Parallel ridges | Improve scanability of aligned list/table rows; keep money strings unchanged. |
| 36 | Crystal symmetry | Establish a quiet, consistent geometry for repeated chart marks; do not imply symmetry in the underlying values. |
| 37 | Wave interference | Use only as a restrained transition texture; never encode two data series with an unexplained wave. |
| 38 | Sine waves | Connect real time-series points where meaningful, without adding unprovided intermediate values. |
| 39 | Periodicity | Animate a user-selected reporting period transition; query Zoho rather than scaling or fabricating values. |
| 40 | Optimisation | Order actionable work by explicit Zoho status/due date rules; disclose sorting and retain manual control. |
| 41 | Packing problems | Group actual item records efficiently on the relevant material/inventory screen; no synthetic stock quantities. |
| 42 | Surface-area-to-volume | Inform performance/geometry choices for small-screen visuals only; never represent a business metric. |
| 43 | Calendar heatmap | Show source-backed document/trip counts by date when the endpoint supplies those records. |
| 44 | Sankey/flow diagram | Show document-state transitions only from recorded workflow events; otherwise mark unavailable. |
| 45 | Line chart | Plot source-backed per-record values over time; preserve each exact Zoho string in labels/table. |
| 46 | Bar comparison | Compare customers, items, document counts or other fields only when the source permits a like-for-like comparison. |
| 47 | Scatter plot | Plot real records against two available source fields; explain both axes and preserve row-level text. |
| 48 | Statistical distribution | Use only when Zoho provides the distribution or underlying records and the method is valid; do not infer it from money. |
| 49 | Treemap | Use only for a source-provided hierarchy and values; provide a complete text/table equivalent. |
| 50 | Network graph | Show verified document/customer/item links for the selected task; omit unavailable or inferred links. |

## Steps

1. Read the current route inventory, `STATUS.md`, Zoho contract and existing
   `ROUTE_DATA_VISUAL_MAP.md`. Identify which routes, fields and workflows
   actually exist; do not start from the missing 475-entry catalogue.
2. Create `NATURE_INTEGRATION_MAP.md` with at least 50 distinct selected cues,
   each mapped to a route, real user task, source/state, original treatment,
   accessible equivalent, motion fallback and verification case. Record
   rejected cues and why. Ensure no duplicate treatment is counted twice.
3. Build the mapped treatments into their real screens in small batches.
   Keep chat, forms and labels as real text/controls. Keep charts and graphs
   in Prompt 07's data/source matrix and build every type relevant to available
   work data—not every type in the reference list.
4. Remove the standalone 475-item Atlas grid/sheet from navigation and do not
   create another all-reference catalogue. If `/atlas` is part of the current
   product contract, repurpose it as a contextual explanation for the cue
   attached to the active task, with a clear return-to-task action. It may
   show only relevant entries, never all inspirations on one page.
5. Preserve verified Atlas records without fabricating missing entries. Keep
   any required owner-data gap visible in `STATUS.md` and mark dependent checks
   `BLOCKED(reason)` or `NOT RUN(reason)`; unrelated task integrations continue.
6. Verify every treatment in normal, Calm/reduced-motion and no-WebGL modes,
   at 375/402/440 px and desktop. Assert source-to-DOM parity, accessible
   labels, keyboard/touch operation, 44 pt targets, contrast and performance.

## Verify

- Automated check confirms at least 50 distinct mapped cues are implemented in
  task surfaces, with no one-page atlas/gallery containing them all.
- Every data-driven mark is traceable to a source field/record. Missing source
  data produces a truthful unavailable/empty state, never a fabricated graphic.
- Charts related to available Zoho-backed work appear in `CHART_MATRIX.md`;
  unsupported types are recorded as unavailable/not meaningful, not populated
  with mock-only synthetic data.
- Playwright covers representative integrations across Today, documents,
  contacts, search/chat, sync/offline and charts; checks DOM parity, keyboard,
  touch, reduced motion, Calm, no-WebGL and no console errors.
- Save evidence in `reports/nature-integration/` and update `STATUS.md` with
  finished, partial and owner-blocked items.

## Done means

- [ ] At least 50 unique reference cues are visibly integrated into relevant
  tasks and verified; the map names each implementation and evidence path.
- [ ] No standalone all-items Atlas/reference sheet is present.
- [ ] All relevant work charts are mapped to real data and built or honestly
  marked unavailable/not meaningful.
- [ ] Full text, interactions and data survive Calm, reduced motion and
  no-WebGL modes.
- [ ] No invented records, analytics, relationships or money calculations.
- [ ] `STATUS.md` records the exact remaining work and evidence.

<!-- END 09_NATURE_ATLAS.md -->

<!-- BEGIN 10_PWA_AND_IPHONE.md -->

# 10 — iPHONE PWA, SELF-TEST AND HOSTING

**Role.** Mobile web engineer for iOS Safari standalone mode.

**Outcome.** Ṛta-BY-KARM installs from Safari to the Home Screen, opens full screen, works offline for its shell and cached documents, and can test itself on the owner's phone.

## Steps
1. **Manifest:** `name` **and** `short_name` exactly `Ṛta-BY-KARM` (the owner's install-metadata rule; do not abbreviate). If iOS truncates the Home Screen label, record the exact truncation in `DECISIONS.md` and keep the name. `start_url` `/today?source=pwa`, `scope` `/`, `display` `standalone`, portrait, theme/background from the new tokens, `lang` `en-IN`, 192/512 and maskable icons, shortcuts (New Invoice, Today, Search).
2. **Icons and splash from the owner's logo only** (scale proportionally, centre on a plain tile with maskable padding; never redraw). Sizes: 180 touch icon, 192, 512, 512 maskable, favicon, startup images for 16 Pro Max, 16 Pro, 16/15, SE with correct media queries.
3. **iOS meta:** `viewport-fit=cover` (zoom stays enabled), apple web-app capable, status bar `black-translucent`, apple title `Ṛta-BY-KARM`, theme colours light/dark, `format-detection telephone=no`. `100dvh` and `env(safe-area-inset-*)`. `overscroll-behavior:none`, `touch-action:manipulation`. Money and numbers stay selectable. Inputs ≥16 px.
4. **Service worker (Workbox via vite-plugin-pwa), production only:** precache shell, scripts, styles, icons, local pdf.js worker; offline fallback that still shows lock and cached documents; **never cache API responses in the SW** (data caching is IndexedDB under lock rules); "New version ready — refresh" toast, never reload while a form is open; version in Settings.
5. **Install coach:** if not standalone, a calm three-step card (Share → Add to Home Screen → keep "Open as Web App" on → Add), "Not now", "Don't show again", repeated in Settings. Write `INSTALL_ON_IPHONE.md` in plain words.
6. **Phone behaviour:** keyboard handling with `visualViewport`; custom pull-to-refresh; swipe-back plus in-app back; sheets trap focus, close on swipe down, lock page scroll; all four safe areas; Web Share for files; long-press copies exact Money text; `navigator.storage.persist()` after sign-in; idle lock.
7. **Best-effort device features** (feature-detected): haptics, tilt (explicit permission), passkeys/Face ID via WebAuthn. Mark real-device behaviour `NOT RUN`.
8. **Push notifications:** optional; `SKIPPED(reason)` if time is short.
9. **Self-test (`/selftest`)** on the real phone: standalone mode, safe areas, storage persistence, IndexedDB, service worker, WebGL2 availability, frame-time sample, motion preference, reduced transparency, lock, clipboard, share, clock/time zone, network state, app version. Each row `PASS`/`FAIL`/`NOT RUN`, with a **Share results** button.
10. **Hosting:** `scripts/deploy.mjs` picks the best free option available, prints the real link only if the deploy succeeded, otherwise the exact commands for a human. Never fabricate a URL.

## Exact-name migration gate

Before calling this prompt done, update and verify the runtime app name in the
actual app source—not only in this prompt or a report. Use exactly
`Ṛta-BY-KARM` in the browser/document title, visible app shell, manifest
`name`/`short_name`, iOS title/install metadata, splash/loading/lock/sign-in and
onboarding surfaces, settings/About, notifications, and current user-facing
install/help copy. Search both source and production build output for alternate
customer-facing names; verify `Ṛ` renders in browser and installed metadata.
Internal package/API/database identifiers and verbatim historical provenance
are not customer-facing labels and should remain stable unless safely required.
If the app source checkout is unavailable, record this gate as
`BLOCKED(reason: app source checkout unavailable)` and do not mark the PWA
release-ready.

## Verify
Playwright WebKit: manifest valid, offline shell loads, install coach appears in non-standalone and not in standalone, keyboard avoids hiding Save, safe-area assertions. Lighthouse mobile recorded. Real-iPhone checks are `NOT RUN` until the owner runs `/selftest`.

## Done means
- [ ] Manifest, icons, meta, SW, install coach, self-test shipped and tested.
- [ ] Runtime UI and metadata use exactly `Ṛta-BY-KARM`; source/build search and glyph checks pass.
- [ ] No secrets in caches.
- [ ] `PWA_REPORT.md` with honest `NOT RUN` entries.

<!-- END 10_PWA_AND_IPHONE.md -->

<!-- BEGIN 11_TESTS_A_FUNCTION_MONEY_ACCESS.md -->

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

<!-- END 11_TESTS_A_FUNCTION_MONEY_ACCESS.md -->

<!-- BEGIN 12_TESTS_B_LOAD_AND_SECURITY.md -->

# 12 — TESTS B: LOAD, RESILIENCE AND SECURITY (OWN SYSTEM ONLY)

**Role.** Performance engineer and defensive security tester. Test only the local proxy and mock; never real Zoho.

## Part 1 — Load and resilience
1. Expected peak: 5 devices × ~30 req/min. Test at 10× and 100×. Write targets before running (list p95 <400 ms on mock; error rate <1% excluding expected 429; zero duplicates; zero crashes; flat memory).
2. k6 (or autocannon; log which): ramp 0→50 VUs, spike 0→500, soak (≥20 min), idempotency storm (200 same key → exactly one document; 200 keys → 200 documents), rate-limit behaviour (friendly 429, never 500).
3. Chaos via mock switches: 401 mid-session, 429 for 60 s, 5xx for 30 s, 8 s latency, dropped connections, token store down, clock skew. Expect friendly messages, backoff, queue retained, no duplicates, no secrets in logs.
4. Browser stress: scroll `/charts` 20×, open/close task-contextual visual explanations 100×, switch theme and tier 100×, lock/unlock 50×; heap must not climb steadily.

## Part 2 — Defensive security pass
5. Static: `npm audit` (production), secret scan including `dist/`, source maps, logs, screenshots and reports; exact product-name scan of customer-facing build output; eslint-plugin-security; semgrep if available; header check (CSP without unsafe-inline/eval, HSTS, nosniff, referrer, permissions policy, frame-ancestors none, `Cache-Control: no-store` on API).
6. Automated attacks as repeatable tests: auth bypass, session fixation/replay, CSRF, brute-force lockout, IDOR on documents/contacts, injection in search and notes, XSS in names/notes/terms/RSS titles, path traversal, malformed JSON/oversized bodies, rejected computed money fields, replayed writes, file/PDF handling.
7. OWASP ZAP baseline against the local app if Docker exists; else `NOT RUN`.
8. Fix every finding (ID, severity, how found, fix, retest evidence). Never hide a finding.
9. Red-team pass after fixes: logic abuse (double payment, wrong customer, date manipulation, races, replay).
10. Verify motion/renderer robustness under load: one shared WebGL context, context loss, hidden-tab pause, governor step-down, Calm/reduced-motion, no-WebGL, and exact DOM/source data parity. Do not treat a decorative FPS result as proof that all routes or data are correct.

## Honesty
The builder's own hacker test is useful but is still the same AI. Recommend a human security review before customers' invoices go through a public link. Never write "fully secure"; write "no known defects after N cycles", with evidence.

## Done means
- [ ] Load, chaos and security reports with raw output saved.
- [ ] All Critical/High fixed or logged `BLOCKED` with reason.
- [ ] `STATUS.md` updated.

<!-- END 12_TESTS_B_LOAD_AND_SECURITY.md -->

<!-- BEGIN 13_RETEST_CYCLES_AND_RELEASE.md -->

# 13 — RETEST CYCLES, RETIRING OLD STYLES, AND RELEASE

**Role.** Release engineer. You close the redesign honestly.

## Steps
1. **Retire old styles only now.** Confirm every route in `STATUS.md` is `DONE` and checked. Then remove retired styles, components, assets and animations; run `verify` after each removal batch. Keep stable internal identifiers. If any route is not migrated, do **not** remove shared old styles it uses, and say so.
2. **`verify-all.mjs`** runs, in order, writing each result into the cycle folder and stopping the cycle at the first FAIL while still recording what ran: clean install + build; typecheck + lint (zero warnings); `scan:money` + scanner self-test; contrast (light/dark); unit/component with coverage thresholds; proxy/mock contract tests; E2E J1–J12 ×3 (iPhone 16 Pro) plus SE and Pro Max smoke; accounting golden tests; axe on every route in all modes + 44 pt; visual regression and route/data parity; exact product-name scan of customer-facing source and built output; performance budgets + Lighthouse; short load + chaos; security tests + audit + secret scan of `dist/`; 50-cue task-integration coverage; PWA checks. Each prints name, `PASS/FAIL/NOT RUN`, duration and raw output path.
3. **Cycles:** Phase A — repeat until three clean cycles in a row (after a FAIL, fix the cause, log it in `CYCLE_LEDGER.md`, restart the count). Phase B — a fresh red-team pass with a different attack style, fix, one more full cycle. Phase C — four more clean cycles with rotated test order and fresh data/browser profiles. **Safety stop:** after 25 total cycles without the required clean runs, stop and write `RELEASE_READINESS.md` as `NOT READY` with the failures.
4. **Flaky hunt:** any test that fails once and passes on re-run is flaky; run it 20×, find the cause, fix, prove 20/20.
5. **Human-needed list (≤10 minutes each):** `/selftest` on the iPhone and Share results; VoiceOver checklist; real Zoho connection and the 20-item `LIVE_CHECKLIST.md`; Add to Home Screen; human security review before public customer links.
6. **`RELEASE_READINESS.md`:** 5-line summary, version/commit, test counts (total/passed/failed/not run), open bugs, known limits, evidence index, exact-brand and route/data visual parity results.
7. **Publish** via `scripts/deploy.mjs` and record the real link or the exact manual commands.
8. **`FINAL_REPORT.md`** per the runbook, plus "What Pratham does next".
9. **Update `STATUS.md`:** final counts, commit, tag.

## Language rules for the report
Never "zero bugs", "perfect", "fully secure", "complete redesign" for a partial migration. Use exact counts and evidence paths. Unavailable physical-device and live-service checks are `NOT RUN`.

## Done means
- [ ] Old styles removed only after full migration, or explicitly retained with reasons.
- [ ] Required clean cycles achieved, or `NOT READY` recorded.
- [ ] Runtime source and built output use exactly `Ṛta-BY-KARM` for every customer-facing name: browser/document title, visible shell, PWA `name`/`short_name`, iOS/install metadata, splash/loading/lock/sign-in/onboarding, settings/About, notifications, and current user-facing guides.
- [ ] Exact Unicode `Ṛ` glyph is verified; searches for alternate customer-facing names in source and built output are saved as raw evidence.
- [ ] If runtime source is unavailable, name migration is explicitly `BLOCKED(reason: app source checkout unavailable)` and release is `NOT READY`; a prompt/document-only change does not satisfy this gate.
- [ ] Visual/data parity is verified or honestly marked `NOT RUN`.
- [ ] `FINAL_REPORT.md` contains no claim without proof.

<!-- END 13_RETEST_CYCLES_AND_RELEASE.md -->

<!-- BEGIN 14_OPTIONAL_NATIVE_IOS_MAC_ONLY.md -->

# 14 — OPTIONAL: NATIVE iOS WRAPPER (ONLY ON A MAC WITH XCODE)

**Role.** iOS engineer. This is optional. The PWA is the product.

## Gate (step 0)
Run `uname -s`, `xcodebuild -version`, `xcrun simctl list devices available`. If not Darwin or Xcode is missing: write `reports/native/NATIVE_NOT_RUN.md` with the output and the sentence "No Mac with Xcode was available, so the native wrapper was not built. The PWA is the product." Set the prompt to `SKIPPED(no Mac)` and **stop**. That is a normal ending.

## Steps (only if the gate passes)
1. Capacitor in `apps/web` (`@capacitor/core`, `cli`, `ios`); display name exactly `Ṛta-BY-KARM`; same web build, no fork. Verify the built iOS display metadata preserves the exact spelling.
2. Plugins from official or well-maintained sources, versions recorded: Haptics, local biometrics (Face ID), Keyboard, Status Bar, Splash Screen, Share, Filesystem (PDFs), App lifecycle (lock). Use real plugins inside the wrapper (`Capacitor.isNativePlatform()`), PWA fallbacks outside. Session secret in the iOS Keychain, not localStorage.
3. Shell rules: portrait only; `NSFaceIDUsageDescription` with a clear reason; ATS on; no tracking; `PrivacyInfo.xcprivacy`; web inspector off in release; blank the view when inactive.
4. Stretch: Dynamic Island Live Activity showing "Syncing with Zoho" / "Sent" — words and counts only, never money. `SKIPPED` if time is short.
5. Apple tests: XCTest for the bridge (Keychain wrapper, lifecycle lock), XCUITest for launch → unlock → Today → quick create → draft.
6. Free install on the owner's own iPhone with an Apple ID; write `INSTALL_NATIVE.md` in plain words, noting free provisioning expires every 7 days.
7. `reports/native/NATIVE_REPORT.md`: what ran (with `xcresult` paths), what did not.

## Done means
- [ ] Gate recorded; either a tested wrapper or an honest skip.

<!-- END 14_OPTIONAL_NATIVE_IOS_MAC_ONLY.md -->

<!-- BEGIN 99_OWNER_GUIDE_READ_ME_FIRST.md -->

# Ṛta-BY-KARM — owner guide

## Current state

This workspace contains the owner prompt pack and dated design evidence. As of
18 October 2026, the actual app source checkout is not present here. The expected
`ऋत-KARM/` folder is absent; the similarly named nested folder contains Git
metadata and `.gitattributes` only. The workspace `STATUS.md` records this
blocker. The historical build note under `redesign-audit/` is not proof of the
runtime state today.

## Before app work

1. Read the workspace-root `README.md`, `CONTINUE-HERE.md`, and `STATUS.md`.
2. Restore or open the intended app working tree, including all saved and
   uncommitted changes. Do not substitute another project or clone.
3. In the restored app checkout, read its own `README.md`, `STATUS.md`, and
   continuation note if present. Preserve existing work and continue its first
   unfinished slice.
4. Read `Prompt/15_OWNER_REDESIGN_OVERRIDE.md`, then `Prompt/00_RUNBOOK.md`,
   then the relevant numbered prompt.
5. Follow the app's own setup and scripts. Run app commands only from that
   checkout and save raw test output in its `reports/raw/`.

## Message to give the builder

`Read the workspace README.md, CONTINUE-HERE.md, and STATUS.md first. Restore or open the actual Ṛta-BY-KARM app checkout and read its own README.md and STATUS.md. Read Prompt/15_OWNER_REDESIGN_OVERRIDE.md and Prompt/00_RUNBOOK.md. Preserve existing work, then continue only the first unfinished app slice. Use the exact customer-facing name Ṛta-BY-KARM. Do not treat historical reports as current test evidence. Save raw output for every PASS; otherwise record NOT RUN or BLOCKED with the reason.`

If work pauses: `Read the workspace CONTINUE-HERE.md and STATUS.md, then the
restored app's own STATUS.md. Continue only from its recorded next step. Keep
the customer-facing name exactly Ṛta-BY-KARM.`

## Product rules

- Zoho Books is the financial source of truth. Render its money strings
  verbatim; the app must not calculate, parse, round, or reformat money.
- Clearly label practice/mock data. Do not assume whether the runtime is in
  practice or live mode until the restored app is inspected.
- Keep the owner's logo unchanged. Preserve accessible text/data equivalents,
  keyboard and touch support, reduced-motion/Calm mode, and a no-WebGL fallback.
- Do not build a single-page catalogue of all nature references. Integrate at
  least 50 valid selected cues into relevant tasks; use only charts that are
  useful and supported by real business data.
- Use exactly `Ṛta-BY-KARM` for every customer-facing app name. Runtime UI and
  metadata must be changed and verified in the actual app source; prompt edits
  alone do not complete that work.
- Real Zoho credentials and the missing nature-list entries are owner-only
  inputs. Never invent them.

## Honest reporting

`PASS` requires a fresh run and saved raw output. Otherwise report `NOT RUN` or
`BLOCKED` with a reason. Device-only, live-Zoho, authenticated screenshot, and
owner visual-review checks must not be claimed unless actually completed with
evidence. The app checkout should maintain its own `STATUS.md`, `BUGS.md`,
`FINAL_REPORT.md`, and raw reports; this workspace status is not a replacement
for those app records.

<!-- END 99_OWNER_GUIDE_READ_ME_FIRST.md -->
