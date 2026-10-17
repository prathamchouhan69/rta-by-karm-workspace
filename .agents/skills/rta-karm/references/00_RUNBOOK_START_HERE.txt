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
