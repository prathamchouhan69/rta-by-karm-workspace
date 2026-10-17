# 12 — TESTS B: LOAD, RESILIENCE AND SECURITY (OWN SYSTEM ONLY)

**Role.** Performance engineer and defensive security tester. Test only the local proxy and mock; never real Zoho.

## Part 1 — Load and resilience
1. Expected peak: 5 devices × ~30 req/min. Test at 10× and 100×. Write targets before running (list p95 <400 ms on mock; error rate <1% excluding expected 429; zero duplicates; zero crashes; flat memory).
2. k6 (or autocannon; log which): ramp 0→50 VUs, spike 0→500, soak (≥20 min), idempotency storm (200 same key → exactly one document; 200 keys → 200 documents), rate-limit behaviour (friendly 429, never 500).
3. Chaos via mock switches: 401 mid-session, 429 for 60 s, 5xx for 30 s, 8 s latency, dropped connections, token store down, clock skew. Expect friendly messages, backoff, queue retained, no duplicates, no secrets in logs.
4. Browser stress: scroll `/charts` 20×, open/close task-contextual visual explanations 100×, switch theme and tier 100×, lock/unlock 50×; heap must not climb steadily.

## Part 2 — Defensive security pass
5. Static: `npm audit` (production), secret scan including `dist/`, source maps, logs, screenshots and reports; exact product-name scan of customer-facing build output; eslint-plugin-security; semgrep if available; header check (CSP without unsafe-inline/eval, HSTS, nosniff, referrer, permissions policy, frame-ancestors none, `Cache-Control: no-store` on API).
6. Automated attacks as repeatable tests: auth bypass, session fixation/replay, CSRF, brute-force lockout, IDOR on documents/contacts, injection in search and notes, XSS in names/notes/terms/RSS titles, path traversal, malformed JSON/oversized bodies, rejected computed money fields, replayed writes, file/PDF handling.
7. OWASP ZAP baseline against the local app if Docker exists; else `NOT RUN`.
8. Fix every finding (ID, severity, how found, fix, retest evidence). Never hide a finding.
9. Red-team pass after fixes: logic abuse (double payment, wrong customer, date manipulation, races, replay).
10. Verify motion/renderer robustness under load: one shared WebGL context, context loss, hidden-tab pause, governor step-down, Calm/reduced-motion, no-WebGL, and exact DOM/source data parity. Do not treat a decorative FPS result as proof that all routes or data are correct.

## Honesty
The builder's own hacker test is useful but is still the same AI. Recommend a human security review before customers' invoices go through a public link. Never write "fully secure"; write "no known defects after N cycles", with evidence.

## Done means
- [ ] Load, chaos and security reports with raw output saved.
- [ ] All Critical/High fixed or logged `BLOCKED` with reason.
- [ ] `STATUS.md` updated.
