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
