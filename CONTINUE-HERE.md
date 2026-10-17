# Continue here — Ṛta-BY-KARM

**Current workspace state (18 October 2026): documentation and design records
are present; the runnable app source is not.** Read this file and the workspace
`STATUS.md` before doing anything else. The status file describes this snapshot;
it is not the app repository's own status.

## Actual stage

- The workspace contains the owner prompt pack and dated redesign/audit records.
- The expected app checkout, `ऋत-KARM\`, is absent. The similarly named nested
  `Ṛta-BY-KARM-reb\` directory contains Git metadata and `.gitattributes` only;
  its recorded `HEAD` has no app source. Do not run app commands from this
  workspace or treat the nested metadata directory as the app.
- The newest saved app-build note is
  `redesign-audit\course-2026-10-17\BUILD-LOG.md`. It records an older
  METRE/bench implementation as saved but uncommitted, several historical
  checks as passing (including a 623/623 Vitest run and production build), and
  authenticated screenshots/owner review as not run. That note attributes the
  screenshot block to competing proxy processes and test-passphrase setup. Its
  source files and raw reports are not available here, so these are historical
  claims, not proof of the current runtime.
- The current workspace design authority is the original FORMWORK direction
  documented in `redesign-audit\formwork-2026-10-17\00-CONCEPT-AND-MAP.md`.
  The older bench/METRE build note is historical, not the implementation to
  resume. The current app's design/code alignment cannot be confirmed without
  its source.
- The prompt pack now requires the exact customer-facing name
  **`Ṛta-BY-KARM`**, task-integrated reference cues, and source-backed,
  business-relevant charts. These are requirements, not proof they are built.

## Next action

Restore or open the actual app working tree, including its uncommitted work and
its own `README.md`, `STATUS.md`, `DECISIONS.md`, `BUGS.md`, and
`reports\raw\`. Preserve that work. Then:

1. Read the app's own `README.md` and `STATUS.md`; compare them with the dated
   evidence above and this workspace's owner rules.
2. Reconcile the actual code with FORMWORK and the latest approved prompt pack.
   Resume the first genuinely unfinished app slice; do not rebuild finished
   work from scratch or copy historical designs.
3. Audit and change every customer-facing runtime name to exactly
   `Ṛta-BY-KARM` (UI, browser/document title, PWA/iOS install metadata, splash,
   lock/sign-in, settings, notifications, and current help). Verify the glyph,
   search source and production output, and save evidence.
4. Re-run the smallest relevant checks from the actual app repository. Mark
   checks `PASS` only with fresh raw output under that repository's
   `reports\raw\`; otherwise use `NOT RUN` or `BLOCKED` with the reason.
5. Update the app's own `STATUS.md` after each completed slice, with evidence
   and the next exact step.

Do not clone, fetch, deploy, or start the app from another folder as a substitute
for restoring the intended checkout. This documentation-only update does not
restore source, run app commands, or build anything. Do not read credentials or
invent missing owner inputs.

## Owner laws to retain

- The app name is exactly `Ṛta-BY-KARM`; FORMWORK is an internal design codename.
- Zoho supplies money strings verbatim; the app does no money arithmetic.
- Mock/practice data stays labelled. Never invent records, test results, or
  owner assets.
- Keep the original logo unchanged, preserve accessible DOM equivalents for
  visuals, and support Calm/reduced motion, no-WebGL, keyboard, and touch.
- Do not make a single-page catalogue of all nature references. Integrate at
  least 50 valid selected cues into relevant tasks; implement only chart types
  supported and useful for actual business data.
- The 401-item nature list and real Zoho credentials remain owner-only inputs.
