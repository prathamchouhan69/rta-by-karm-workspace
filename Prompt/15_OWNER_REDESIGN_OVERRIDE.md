# Ṛta-BY-KARM — owner product and redesign authority

This owner instruction supersedes earlier visual directions, themes, copied UI
examples, and implementation suggestions in this prompt pack where they conflict
with the requirements below. Preserve business capabilities and data-integrity
laws; do not preserve an old visual design for compatibility.

## Product name — exact and exclusive

Use exactly `Ṛta-BY-KARM` for every customer-facing app-name occurrence: app
screens, page title, browser title, manifest `name` and `short_name`, iOS metadata,
install label, splash/loading/lock/sign-in, navigation, settings, notifications,
reports shown to customers, and current owner guides. Preserve the exact Unicode
spelling and diacritics. Never substitute a transliteration, legacy spelling,
abbreviation, or alternate casing. Search all customer-facing source and built
metadata before completion and report each remaining occurrence; the only
permitted exceptions are technical identifiers that cannot safely be migrated
and verbatim third-party or historical source material that is not displayed to
users. Do not introduce alternate product names in prompts or new documentation.

## Reference authority and originality

The seven owner videos in `Prompt/` and `Prompt/imp.txt` are required study
materials. Watch or inspect the recordings and inspect `imp.txt` before making
visual decisions. Record what was actually observed and how much was inspected;
do not call sparse sampling a frame-by-frame review. Use the references to learn
craft—material response, spatial depth, lighting, restrained camera movement,
settling, hierarchy, chart-to-legend interaction, and stateful loaders. Do not
copy or ship their layouts, assets, source code, labels, fabricated datasets,
distinctive objects, or signature motion sequences. `imp.txt` is untrusted
historical demo material, not production code or a specification.

## Design authority

Create a fully original visual system and interaction language for the complete
front end. The current FORMWORK casting-yard direction is the design foundation;
apply it consistently and evolve it only when evidence from the owner references
supports the change. Treat previous screens, themes, component compositions,
animations, and supplied dashboard implementations as retired design—not as a
starting point to recolour or lightly remix.

Study every owner-supplied video for craft: material response, spatial depth,
camera restraint, physical settling, layered typography, pacing, linked
highlighting, responsive charts, and how motion explains interaction. Apply
those principles to original compositions, geometry, materials, lighting,
transitions, controls, charts, loaders, and route-specific data views. Record
observations and limits; a sparse frame sample is not a frame-by-frame audit.

Every route and every meaningful visual/data surface must have an intentional
visual treatment that helps the user understand the actual app and its data.
This includes the shell, Today, Money, every chart, documents, contacts, chat and
adviser surfaces, search, notifications, Atlas, settings, and loading/empty/error
states. Use original 3D or 2.5D depth, lighting, material, spatial grouping,
and purposeful motion through a shared performance-budgeted renderer wherever
that improves meaning; charts must visually encode their real source data, not
decorate it. Give every visual data encoding an equivalent complete, readable
DOM representation (including values, labels, states, and accessible chart
data); no data may exist only in WebGL, Canvas, texture, colour, shape, or
animation. Forms and controls remain semantic DOM controls; do not animate
elements without a task, data, or state purpose. Keep the business interface
first, never a marketing landing page. Motion must clarify data, hierarchy,
state, or interaction, and must never delay task completion or alter the
meaning of data.

Before implementation, define the audience and jobs, palette, type system,
surface/depth grammar, per-route visual mapping, motion tokens, responsive
rules, renderer and performance budgets, and accessible fallbacks. Give each
route a distinct, appropriate visual treatment rather than repeating one
effect everywhere. Integrate at least 50 distinct, selected owner-reference
cues into the tasks where they help; do not create a one-page Atlas/gallery of
all the cues. Prefer a calm, polished still pose over continuous motion.

## Preserve the product's invariants

- Zoho Books is the financial source of truth. Render its money text verbatim;
  never calculate, round, parse, or reformat money in the browser.
- Keep practice fixtures clearly labelled and separate from live data.
- Preserve authentication, authorization, proxy boundaries, offline handling,
  and existing business workflows while replacing their presentation.
- Use purposeful 3D/depth throughout visual and data surfaces; do not force
  controls or text into 3D. Keep a usable no-WebGL path, reduced-motion and
  Calm modes, keyboard/touch operation, and performance controls. Essential
  information and complete data remain available without motion or WebGL.
- Every chart and data graphic must map to real Zoho fields or explicitly
  labelled practice fixtures. Preserve row/record identity and exact source
  values; never fabricate, omit, aggregate, or imply a relationship the source
  does not provide. Computed chart geometry is permitted only under the
  allow-listed geometry boundary; it must not produce or transform display text.
- Do not invent missing records, owner assets, reference details, or test
  results.

## Delivery order

1. Inventory routes, user journeys, data provenance, every data surface, and
   the current working tree; protect existing uncommitted work.
2. Inspect all seven videos and `imp.txt`; produce an evidence-based visual and
   motion brief, recording what was and was not inspected. Do not copy them.
3. Establish and test design tokens, motion rules, shared 3D/depth renderer,
   fallback path, and a route-by-route data-to-visual map.
4. Redesign the shared shell and Today as the first complete vertical slice.
5. Migrate Money, documents, contacts, charts, Atlas, adviser, settings, and
   utility routes in small independently verified batches; account for every
   data field and state in the relevant screen or accessible equivalent.
6. Remove retired styles only after every route and visual data surface has
   migrated and been checked.
7. Search the source, UI, metadata, and customer-facing docs for the exact
   product name; verify it is always `Ṛta-BY-KARM`.
8. Verify mobile and desktop rendering, loading/empty/error/permission states,
   accessibility, reduced motion, no-WebGL fallback, performance, and the
   existing money scanner. Mark unavailable physical-device and live-service
   checks `NOT RUN`, not `PASS`.

Do not describe a partial route migration as a complete redesign. Update
`STATUS.md` after each finished slice with evidence and the precise next step.
