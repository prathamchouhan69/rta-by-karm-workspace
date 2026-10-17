# FORMWORK — original concept, DNA report and experience map
Date: 2026-10-17 · App: **Ṛta-BY-KARM** · Internal codename: FORMWORK (never user-visible)

Owner order for this pass: build a completely original, high-end, realistic 3D motion-design
front end from zero. Every prior design is **forbidden visual source**.

## 0. Forbidden source (inventoried, so the distinctness is provable)

| Rejected / retired | Its look — none of it may appear here |
|---|---|
| abyssal / nautilus "living world" | night `#0b0d12` glow-forest, nautilus dock, Reef lists, Living Paper, Chladni, phyllotaxis, bioluminescent emerald |
| STRATA (D-042) | contour rings, seam lines, stepped strata, copper notes, field-observatory rail |
| COURSE yard (D-055, twice rejected) | Dhoop `#E7DCCD` / Chandni `#14120F`, geru red, river teal, sandstone diorama, furrowable sand heap |
| METRE / instrument bench (D-055, live-but-rejected by this order) | Lamp `#101410` / Enamel `#E6E5DC`, brass, scarlet, metronome, odometer rollers, catalogue drawers, gauge dials, Bricolage + Spline Sans Mono |
| Video-look imports (D-053/D-054) | three tall glass cards, pointillist dither donut, liquid particle sculpture, pixel-text fill, tetris stacker |
| The recordings themselves | their layouts (nav-top/copy-bottom card, 3×2 dark grid), their palettes (cream/sepia, black+emerald/pink/gold, orange-on-black), their objects |

Typefaces retired with those directions: Space Grotesk, Inter, JetBrains Mono, Instrument
Serif, Archivo, Martian Mono, Bricolage Grotesque, Spline Sans Mono.

## 1. Creative DNA (measured, not guessed)

The full per-scene measurement lives in `../course-2026-10-17/01-AUDIT-AND-DNA.md`
(8,774 frames through ffmpeg; declared source constants). What makes the references feel
expensive is **not** their geometry count. It is eleven transferable laws, and FORMWORK
obeys every one of them with its own materials:

1. **One hero, alive at rest.** A single object carries the screen; everything else is still.
2. **Touch is a local, reversible disturbance.** The pointer pushes, the field springs home.
   Answer in <100 ms, settle in 200–500 ms (τ ≈ 100–170 ms).
3. **Weight comes from springs, not durations.** Reorder 0.38 s / bounce 0.16; lift 0.26 s /
   bounce 0.32 — the *lift* is bouncier than the *landing*.
4. **Anticipation is tiny.** 9° → 1°, +10 px, 1.8 % squash. Nothing telegraphs like a cartoon.
5. **Stagger is structure.** 40 ms × depth for transform, 180 + 90 ms × depth for opacity.
6. **Depth is cheap.** perspective 760–1400 px, ±3–4° lean, ±8 px layer parallax, a glare
   spot that follows the pointer.
7. **Light carries meaning.** Unfocused things dim to 0.22–0.3 alpha; emphasis is lighting,
   not colouring-in.
8. **Data stays legible.** Text is real DOM, selectable, never painted into a canvas.
9. **Scroll is a timeline, not a trigger.** Progress eases 0.18/frame toward scroll position.
10. **Ambient life is unsynchronised.** Independent 2–5 s ticks, never a shared beat.
11. **Calm is a still, lit pose** — zero durations, information intact.

## 2. Original concept: the casting yard

Karm Enterprises sells the things that get **cast**: sand, stone dust, cement, paver blocks,
RCC pipes, and the trucks that carry them. FORMWORK is the world of the mould and the pour.
Not a forest, not a desk, not a bench of brass instruments — a **yard of concrete under a
low, raking sun**.

- **Central metaphor.** Every record is a cast unit. Every card is a slab. Every route is a
  different way the yard is laid out that morning.
- **3D world (one WebGL context, ~6 draw calls).** An instanced field of interlocking paver
  blocks on a ground plane, lit by one warm key low on the horizon plus a cold sky fill,
  with analytic contact darkening (no shadow maps), per-instance albedo wear from in-shader
  noise, and a shallow drift of dust motes in the beam. Camera sits at ~14° elevation and
  parallaxes to pointer and scroll.
- **Materials read as real** because of three things only: a wrapped diffuse term, a tight
  specular that *only* appears where the surface faces the key, and edge wear that brightens
  the arrises. That is what makes cheap geometry look like a product render.
- **Motion personality: "pour, cure, lift."** Units drop from above and settle with a heavy
  spring; slabs lift toward the finger and clack back; a cure-glow creeps across a stack on
  its own unsynchronised clock. Nothing bounces for fun.
- **Two worlds.** Night = **Pour** (the yard after the pour, lamp-lit, cool graphite, one
  hot oxide accent). Day = **Cure** (damp concrete in morning light, warm pale grey, ink).
- **Type.** Display **Syne** (architectural, wide-set 700/800 — reads like formwork lettering),
  body **Hanken Grotesk**, data **DM Mono** (tabular, so Zoho's figures column up).
  None of these appear in any retired direction.
- **Accent.** Iron **oxide `#C7521F`** (the colour of the sand and the wet cement set), with
  a cold **sky-fill steel `#7C93B8`** for structure. The owner's logo swirl `#4F669C` stays
  locked to the logo and is never used as an accent.

## 3. Hard constraints honoured

- **Money law.** Zero arithmetic. Every figure is Zoho's own string through the existing
  `Money` component; only *counts* are computed. `src/world/**` and `src/motion/**` never
  receive money (world-boundary test). `npm run scan:money` stays green.
- **One WebGL context** (Intel HD 5500, i3-5005U): the cast field takes the lease and yields
  it to ChartStage on `/money` and `/charts`; DPR ≤ 2 (1.5/1.0 on low tiers); pauses when
  hidden; `?flat` and lost-context fall back to a Canvas-2D/CSS yard; Calm holds one still frame.
- **Logo.** The owner's file, unchanged, SHA-256 recorded. Never redrawn.
- **Accessibility.** WCAG 2.2 AA asserted by script, not by eye; 44 pt minimum hit areas;
  real text; focus order; both worlds measured for contrast.
- **UK English.** The only customer-facing app name is **Ṛta-BY-KARM**, in this exact spelling.

## 4. Experience map

| Route | Station in the yard | Hero | What moves | What stays text |
|---|---|---|---|---|
| Boot / splash | the pour | Concrete fills a mould and the wordmark casts into it | 1.1 s pour, 40 ms stagger | "Ṛta-BY-KARM" |
| Lock | the gate | Slab drops, then lifts on a correct passphrase | spring 0.32 s / bounce 0.2 | all copy |
| `/today` | the yard at dawn | One lifted unit under the low key; the field breathes | pointer ripple, cure ticks | counts, source line, times |
| `/money` | the stack wall | Units stack into rows as Zoho pages arrive (counts only) | lease yields to ChartStage | every Zoho figure verbatim |
| `/documents` | the open crates | Crate grid, one crate slides toward the chosen kind | 40 ms depth stagger | kind names, source meta |
| `/charts` | the test rig | ChartStage owns the GPU; the yard becomes printed texture | per-card scenes | axis + tooltip strings |
| `/atlas` | the scree slope | Canvas-2D scatter under selectable labels | focus shift on select | every teacher's text |
| `/studio` | the sample board | Every part in every state, both worlds, Calm, 100/150/200 % | parameter sliders | labels |
| `/selftest` | the gauge shed | Owner's phone readings | none | PASS/FAIL/NOT RUN |

Global: dock = five cast stations with the logo as the pour button; island row = the day's
status; search sheet, agent, notifications, install coach, offline queue — all kept, all
re-dressed. Route change = 320 ms camera dolly + the new station pours in.
