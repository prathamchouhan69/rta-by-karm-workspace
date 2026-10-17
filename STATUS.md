# Workspace status — Ṛta-BY-KARM

**Updated:** 18 October 2026
**Scope:** this documentation/design workspace only. This is not the runnable
app's `STATUS.md`.
**Overall:** the last recorded app stage is a saved, uncommitted 17 October
implementation snapshot with selected checks reported passing and authenticated
visual review still blocked. Current runtime state cannot be confirmed because
the actual app checkout is absent from this workspace snapshot. This status
update is documentation-only; no checkout restore, app command, or build was
performed.

| Slice | Routes/files | State | Evidence path | Next step |
|---|---|---|---|---|
| Workspace owner guidance | `AGENTS.md`, `README.md`, `CONTINUE-HERE.md`, this file | DONE | These workspace files | Keep aligned with owner orders and verified checkout state |
| Prompt pack alignment | `Prompt/` canonical prompts, merged pack, active `rta-karm` references | DONE (instructional only) | `Prompt/15_OWNER_REDESIGN_OVERRIDE.md`; `Prompt/09_NATURE_ATLAS.md`; `Prompt/07_MONEY_DASHBOARD_AND_CHARTS.md`; `Prompt/ALL_PROMPTS_IN_ONE.md` | Execute against the real app checkout when restored |
| Current app source and app-owned status | Expected `ऋत-KARM\` | BLOCKED (checkout unavailable) | Nested `Ṛta-BY-KARM-reb\` contains only `.git` and `.gitattributes`; recorded `HEAD` lists only `.gitattributes` | Restore/open the intended app worktree, preserving all saved and uncommitted work |
| Last recorded implementation snapshot | Historical 17 October build note; not present source | NOT RUN (cannot verify current runtime) | `redesign-audit\course-2026-10-17\BUILD-LOG.md` | Compare the real checkout against its claims; do not treat the note as current source |
| Current design implementation | FORMWORK concept is documented; current app code is unavailable | BLOCKED (implementation alignment unverified) | `redesign-audit\formwork-2026-10-17\00-CONCEPT-AND-MAP.md`; see also `AGENTS.md` | Audit actual routes and code against FORMWORK before resuming implementation |
| Authenticated visual review | Historical note says it did not run | BLOCKED (source and runtime unavailable) | `redesign-audit\course-2026-10-17\BUILD-LOG.md` | After restoring app, use a controlled test vault/proxy setup and save fresh evidence |
| Exact runtime app-name migration | All user-visible app surfaces and generated output | BLOCKED (source unavailable) | Required by `Prompt/02_FOUNDATION_AUDIT_AND_GUARDRAILS.md`, `Prompt/10_PWA_AND_IPHONE.md`, and `Prompt/13_RETEST_CYCLES_AND_RELEASE.md` | Change and verify every customer-facing runtime name as exactly `Ṛta-BY-KARM` |
| Current build, typecheck, tests, and money scan | Actual app repository | NOT RUN (checkout and raw outputs unavailable) | No app `package.json`, source tree, or current `reports\raw\` is present | Run targeted checks only after restoring the actual checkout; save raw output there |
| Live Zoho and complete nature dataset | Owner-provided credentials and 401-item list | BLOCKED (owner inputs) | `Prompt/03_ZOHO_PROXY_AND_MOCK_AUDIT.md`; `Prompt/09_NATURE_ATLAS.md` | Keep practice mode; do not invent credentials or missing nature entries |

## Last-known app notes (historical, not current verification)

The 17 October `BUILD-LOG.md` records an older METRE/bench build as saved
uncommitted work. It reports TypeScript clean, lint clean with one pre-existing
warning, zero-math scan pass, Vitest 623/623, and production build pass. It
explicitly says the authenticated screenshot pass and owner visual review were
not run; the screenshot attempt was blocked by competing proxy processes and
passphrase setup. The referenced source and raw evidence are not present in this
workspace snapshot. These dated results are historical claims, not proof of the
current app state or authority to resume that superseded visual direction.

The older `redesign-audit/REPORT-2026-10-17.md` describes an earlier redesign-v2
snapshot and different test counts. Do not merge its claims with the later
`BUILD-LOG.md` results or treat either record as a fresh verification run.

The current documented visual direction is FORMWORK. Its presence in design
records does not establish that it is implemented in the unavailable app source.
Likewise, the prompt pack's exact-name and chart/reference requirements are
instructions, not completed runtime work.

## Resume gate

Do not mark any app slice complete from this workspace alone. Once the actual
app checkout is restored, read its own `README.md` and `STATUS.md`, preserve its
working tree, reconcile its status with this record, and update that app-owned
status file with fresh evidence after each slice. No app code/build/test claim is
made by this workspace status.
