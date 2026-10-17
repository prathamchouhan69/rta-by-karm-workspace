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
