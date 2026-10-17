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
