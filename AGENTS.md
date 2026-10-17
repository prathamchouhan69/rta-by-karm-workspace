# AGENTS.md — Ṛta-BY-KARM workspace (self-contained: everything an agent needs lives here)

**What this is:** the **Ṛta-BY-KARM** workspace for owner guidance, prompts, and
design evidence. In this 18 October 2026 snapshot, the runnable app source is
not present. The expected `ऋत-KARM/` path is absent; the similarly named nested
directory contains Git metadata and `.gitattributes` only. See the root
`README.md`, `CONTINUE-HERE.md`, and `STATUS.md` for the verified state and
restore gate. The exact and only customer-facing app name is **Ṛta-BY-KARM**.
FORMWORK is an internal design codename, never a product label.

## Folder map

| Path | What it is |
|---|---|
| `Prompt/` | The owner’s build instructions: `15_OWNER_REDESIGN_OVERRIDE.md`, `00_RUNBOOK.md`, prompts 01–14, the owner guide, and the merged prompt pack. |
| `Prompt/` videos + important files | **MOST IMPORTANT.** The seven owner videos and prompt files are protected references. Never delete, overwrite, or ignore them. |
| `ऋत-KARM/` | Expected app checkout (`apps/web`, `apps/proxy`, mock Zoho, shared packages); absent from this snapshot. Do not treat the nested metadata-only directory as the app. When restored, read its `README.md` and `STATUS.md` first. |
| `ऋत-KARM/00-KEEP/` | Expected retained-owner-assets folder in the app checkout; unavailable in this snapshot. |
| `ऋत-KARM/inputs/`, `ऋत-KARM/assets/` | Expected owner-input folders in the app checkout; unavailable in this snapshot. Do not invent missing owner material. |
| `.agents/skills/` | Installed agent skills — auto-discovered by ZCode for ANY account opening this folder. `rta-karm` = the build brain (prompt pack as references); `ui-ux-pro-max` = design search brain (Python); `karm-design-agent` = design pipeline; plus design/UI/browser skills. |
| `skills/`, `Ṛta'sBranwise.skill` | Human-readable archive and the packaged `.skill` (zip). `skills/karm-os` is the superseded older skill — prefer `rta-karm`. |

## Most important files (read these FIRST, above everything else)

1. **Video files** (`.mp4`, `.mov`, `.webm`): inspect them before visual design/build work and record what was actually inspected. Treat craft as evidence; do not copy source layouts, assets, code, labels, data, or signature motion.
2. **Important files in `Prompt/`**: read `15_OWNER_REDESIGN_OVERRIDE.md`, then `00_RUNBOOK.md`, the first unfinished numbered prompt, and `99_OWNER_GUIDE_READ_ME_FIRST.md` as needed. `ALL_PROMPTS_IN_ONE.md` is a generated mirror. `imp.txt` is historical demo material for analysis only, never production source.
3. **Never move, rename, compress or delete** these files. Any change to them needs an explicit owner order recorded in `DECISIONS.md`.

## Standing laws (never break these)

1. **ZERO-MATH money law** — every money figure on screen is Zoho Books' own text,
   verbatim. The app never computes money; a zero-math scanner fails the build.
   Specimens are labelled SPECIMEN until live Zoho connects.
2. **Truth law** — PASS only with saved raw output (evidence in `reports/raw/`), else
   NOT RUN. Never claim "zero bugs" or "fully secure". Judgement calls go in
   `DECISIONS.md`, failures in `BUGS.md`.
3. **Design law:** the current documented visual direction is the FORMWORK
   casting-yard plan at `redesign-audit/formwork-2026-10-17/00-CONCEPT-AND-MAP.md`.
   The app source previously cited as corroboration is unavailable in this
   snapshot, so runtime alignment is unverified. Apply route-specific,
   purposeful depth/3D motion and data visualisation across the full product, grounded
   in the seven owner videos and `Prompt/imp.txt` as craft references only; never copy
   their source compositions or fabricated data. Every graphic has a complete DOM
   equivalent. Older directions are history, not current visual sources. Preserve the
   original logo, reduced-motion/accessibility support, iPhone-first layout, Zoho-only
   money, truth labels, UK English, owner-input boundaries, and exact product name
   **Ṛta-BY-KARM**.
   When restored, the app's own `ऋत-KARM/STATUS.md` must record implementation
   progress. Workspace `STATUS.md` records the present source-unavailable blocker.
4. **Runtime brand migration is release-blocking:** when the app checkout is
   restored, update every customer-facing app name in source and built output
   to exactly `Ṛta-BY-KARM`, including browser title, manifest `name` and
   `short_name`, iOS metadata, install/splash/lock/sign-in screens, visible shell,
   settings and current user guides. Verify the `Ṛ` glyph and search for stale
   names. This migration is currently blocked; never report it complete until
   actual source and built output have been checked.
5. **UK English everywhere.** India GST is Zoho's job, not the app's.
6. **Secrets** never in code, logs, tests or reports (`.env` is git-ignored).

## Ports (owner order 2026-10-11, DECISIONS.md D-016)

Web dev server **:6060 — NEVER :5173** · proxy :4040 · mock Zoho :4010 ·
preview + deploy tunnel :4173 (`node scripts/deploy.mjs`).

## How to continue the build

**Resuming on this PC? Read the root `README.md`, `CONTINUE-HERE.md`, and
`STATUS.md` first.** They describe the actual workspace snapshot. The app's own
continuation note and status are unavailable until its checkout is restored.

1. Read `Prompt/15_OWNER_REDESIGN_OVERRIDE.md`, then `Prompt/00_RUNBOOK.md`.
2. When the app checkout is present, read its `README.md` and `STATUS.md`; resume
   the first app slice that is not DONE/BLOCKED/SKIPPED.
   **Never restart finished work.** If the owner says nothing else, that one instruction
   is the whole brief: nobody is available to answer questions.

## Environment (already machine-wide on this PC, `C:\ProgramData\KARM-Toolchain`)

Node + npm, Python 3.12 (for the ui-ux-pro-max search brain), and Playwright
browsers are machine-wide. App scripts (`npm run dev` / `npm run build` /
`npm run verify`) can only run from the actual app checkout after it is restored.
Docker and offline LLMs are deliberately NOT installed (owner order).

## Missing — owner-only inputs (do not invent)

- The **401-item nature list** remains an owner-only input. Do not invent its
  contents or build a one-page Atlas catalogue; integrate at least 50 supplied
  reference cues into relevant tasks as directed by Prompt 09.
- **Real Zoho credentials** — owner follows `ऋत-KARM/SETUP_ME.md`; app stays in PRACTICE
  MODE (mock) until then.
- Lone Walker mascot — superseded (DECISIONS.md D-001); do not build.

## NOT part of this workspace

`C:\KARM-Agents\` is an older duplicate of this project and
`C:\KARM-AI-Workstation\` a retired sibling app — never build from or into them.