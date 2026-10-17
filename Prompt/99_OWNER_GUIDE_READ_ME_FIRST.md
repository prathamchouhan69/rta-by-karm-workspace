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
