---
name: rta-karm
description: Build, continue, test, and release the Ṛta-BY-KARM Zoho Books-backed iPhone PWA for Karm Enterprises. Use when the user mentions Ṛta-BY-KARM, Karm Enterprises, its prompt pack, or asks to build, continue, test, or release the app.
---

# Ṛta-BY-KARM build guide

The current, authoritative build instructions live in the workspace `Prompt/`
folder. The `references/` files mirror those prompts for skill-only contexts;
keep the mirror synchronised and resolve any conflict in favour of the current
workspace `Prompt/` files.

## Start every build session

1. Read workspace `AGENTS.md`.
2. Read workspace-root `README.md`, `CONTINUE-HERE.md`, and `STATUS.md`.
3. Read `Prompt/15_OWNER_REDESIGN_OVERRIDE.md`, then `Prompt/00_RUNBOOK.md`.
4. The current snapshot has no app source checkout. Do not restore a checkout,
   build the app, or run app checks unless the user asks. If a later task
   provides the actual app tree, read its own `README.md` and `STATUS.md` and
   continue only from its recorded unfinished slice.
5. Read the current numbered prompt in `Prompt/` fully before implementation.

## Product and design invariants

- The only customer-facing product name is exactly `Ṛta-BY-KARM`. Keep this
  spelling in UI, metadata, install surfaces, reports and current guides.
- Study the seven `Prompt/*.mp4` videos and `Prompt/imp.txt` for craft only.
  They are references, not source layouts, copy, assets, code, or data. Record
  inspection limits. Never ship fabricated demo values or component code from
  `imp.txt`.
- Apply the current FORMWORK design direction with original, purposeful,
  route-specific depth/3D motion and visualisation. Every meaningful data
  surface must map to source data and have a complete, accessible DOM
  equivalent. Keep motion responsive and secondary to work.
- Zoho Books is the financial source of truth. Display its money strings
  verbatim; never calculate, round, parse, or reformat money in the app.
- Label mock/practice fixtures. PASS requires saved raw evidence; otherwise
  report NOT RUN with the reason. Never claim zero bugs or full security.
- Preserve the owner's original logo unchanged, the reduced-motion/Calm path,
  no-WebGL fallback, keyboard/touch access, UK English, and secrets boundary.

Use current prompt files for requirements. Use the app's own status and fresh
raw evidence only when its source is available. Treat dated audit/build notes as
historical claims, not current runtime verification.
