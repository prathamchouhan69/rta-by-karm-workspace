# 10 — iPHONE PWA, SELF-TEST AND HOSTING

**Role.** Mobile web engineer for iOS Safari standalone mode.

**Outcome.** Ṛta-BY-KARM installs from Safari to the Home Screen, opens full screen, works offline for its shell and cached documents, and can test itself on the owner's phone.

## Steps
1. **Manifest:** `name` **and** `short_name` exactly `Ṛta-BY-KARM` (the owner's install-metadata rule; do not abbreviate). If iOS truncates the Home Screen label, record the exact truncation in `DECISIONS.md` and keep the name. `start_url` `/today?source=pwa`, `scope` `/`, `display` `standalone`, portrait, theme/background from the new tokens, `lang` `en-IN`, 192/512 and maskable icons, shortcuts (New Invoice, Today, Search).
2. **Icons and splash from the owner's logo only** (scale proportionally, centre on a plain tile with maskable padding; never redraw). Sizes: 180 touch icon, 192, 512, 512 maskable, favicon, startup images for 16 Pro Max, 16 Pro, 16/15, SE with correct media queries.
3. **iOS meta:** `viewport-fit=cover` (zoom stays enabled), apple web-app capable, status bar `black-translucent`, apple title `Ṛta-BY-KARM`, theme colours light/dark, `format-detection telephone=no`. `100dvh` and `env(safe-area-inset-*)`. `overscroll-behavior:none`, `touch-action:manipulation`. Money and numbers stay selectable. Inputs ≥16 px.
4. **Service worker (Workbox via vite-plugin-pwa), production only:** precache shell, scripts, styles, icons, local pdf.js worker; offline fallback that still shows lock and cached documents; **never cache API responses in the SW** (data caching is IndexedDB under lock rules); "New version ready — refresh" toast, never reload while a form is open; version in Settings.
5. **Install coach:** if not standalone, a calm three-step card (Share → Add to Home Screen → keep "Open as Web App" on → Add), "Not now", "Don't show again", repeated in Settings. Write `INSTALL_ON_IPHONE.md` in plain words.
6. **Phone behaviour:** keyboard handling with `visualViewport`; custom pull-to-refresh; swipe-back plus in-app back; sheets trap focus, close on swipe down, lock page scroll; all four safe areas; Web Share for files; long-press copies exact Money text; `navigator.storage.persist()` after sign-in; idle lock.
7. **Best-effort device features** (feature-detected): haptics, tilt (explicit permission), passkeys/Face ID via WebAuthn. Mark real-device behaviour `NOT RUN`.
8. **Push notifications:** optional; `SKIPPED(reason)` if time is short.
9. **Self-test (`/selftest`)** on the real phone: standalone mode, safe areas, storage persistence, IndexedDB, service worker, WebGL2 availability, frame-time sample, motion preference, reduced transparency, lock, clipboard, share, clock/time zone, network state, app version. Each row `PASS`/`FAIL`/`NOT RUN`, with a **Share results** button.
10. **Hosting:** `scripts/deploy.mjs` picks the best free option available, prints the real link only if the deploy succeeded, otherwise the exact commands for a human. Never fabricate a URL.

## Exact-name migration gate

Before calling this prompt done, update and verify the runtime app name in the
actual app source—not only in this prompt or a report. Use exactly
`Ṛta-BY-KARM` in the browser/document title, visible app shell, manifest
`name`/`short_name`, iOS title/install metadata, splash/loading/lock/sign-in and
onboarding surfaces, settings/About, notifications, and current user-facing
install/help copy. Search both source and production build output for alternate
customer-facing names; verify `Ṛ` renders in browser and installed metadata.
Internal package/API/database identifiers and verbatim historical provenance
are not customer-facing labels and should remain stable unless safely required.
If the app source checkout is unavailable, record this gate as
`BLOCKED(reason: app source checkout unavailable)` and do not mark the PWA
release-ready.

## Verify
Playwright WebKit: manifest valid, offline shell loads, install coach appears in non-standalone and not in standalone, keyboard avoids hiding Save, safe-area assertions. Lighthouse mobile recorded. Real-iPhone checks are `NOT RUN` until the owner runs `/selftest`.

## Done means
- [ ] Manifest, icons, meta, SW, install coach, self-test shipped and tested.
- [ ] Runtime UI and metadata use exactly `Ṛta-BY-KARM`; source/build search and glyph checks pass.
- [ ] No secrets in caches.
- [ ] `PWA_REPORT.md` with honest `NOT RUN` entries.
