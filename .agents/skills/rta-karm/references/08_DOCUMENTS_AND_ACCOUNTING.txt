# 08 — DOCUMENTS, CONTACTS AND ACCOUNTING WORKFLOWS

**Role.** Product designer-engineer for high-stakes forms and lists. A site manager must complete an invoice one-handed in poor light without ever doubting a number.

**Outcome.** Redesigned Documents, Contacts and Offline flows. **Presentation changes; workflow, validation, idempotency and Zoho contracts do not.** Migrate in batches: (a) list + view, (b) editor, (c) actions + PDF, (d) offline queue UI, (e) contacts, (f) T&C and settings.

## Preserve exactly
- **Kinds:** Tax Invoice, Quotation, Sales Order, Delivery Challan, Credit Note, Customer Payment, Retainer Invoice, Purchase Order, Bill, Vendor Credit, Vendor Payment, Expense, Journal as full screens; reports Zoho's API lacks (balance sheet, P&L, trial balance, GST ledger, audit trail, statements) as honest "Lives in Zoho Books" tiles with **Open in Zoho Books**. Full + tile kinds ≥20 in `DOCUMENT_MATRIX.md`.
- **Editor (raw inputs only):** customer search, dates, terms, place of supply (Zoho list), reference, line items (item search; quantity and rate typed as text; rate prefilled from Zoho text; discount typed; tax **chosen** from Zoho's list), notes, T&C set. While editing, **no total is ever shown**; the exact sentence "Total will be calculated by Zoho Books" stays visible with **Save as draft in Zoho**. After Zoho replies, show the saved document with every figure as Zoho text.
- **Actions only as Zoho offers them** (send, mark sent, void, clone, convert estimate/sales order → invoice, record payment, apply credit, delete draft). Destructive actions need confirmation by typing the document number or long-press, in plain words. Every write carries an idempotency key.
- **PDF:** Zoho's own PDF via the proxy in a local pdf.js viewer; Web Share and Download. Never generate your own invoice PDF.
- **T&C sets:** ≥3 per kind, owner's own clauses word for word if found (quotation has eight numbered clauses); otherwise labelled drafts "DRAFT – owner to review. Not legal advice." No money amounts inside T&C text.
- **Offline queue:** raw inputs + key in IndexedDB; "Waiting for Zoho" state with no totals; ordered send; 4xx shows Zoho's message and keeps the item; 5xx retries with growing delays up to 8; cached documents readable offline with an "As of …" label.
- **Lists:** virtualised, instant search, status pills, pull to refresh, infinite scroll.
- **Contacts:** Zoho's outstanding receivable and unused credits as text; vendor equivalents.

## Design brief for this area
- Document view reads like a trustworthy statement: figures aligned, labels exact, status obvious, actions grouped by risk.
- Editor: one-handed reachability, sticky save area that survives the iOS keyboard (`visualViewport`), line-item entry optimised for repeated materials, large steppers, clear error placement.
- Visuals: give document kinds, lists, status, queue progress and record detail original FORMWORK depth/material treatments that make the real workflow and source state easier to understand. Do not turn every row into an animated object or repeat the same glass-folder treatment everywhere.
- Motion: list rows use restrained, purposeful depth; opening a document may use an original shared-element transition; every movement has a Calm/reduced-motion still equivalent; never animate, transform or render figures through a canvas.
- Data coverage: map every displayed document/contact/queue field to its Zoho or local source. Keep every record, exact figure string, status, label and error available as selectable DOM text; visual groupings may not imply unprovided relationships or hide items.
- States: loading, empty, error, permission, offline, practice, conflict.

## Verify (against the mock; say so in reports)
Journeys J2–J6 three times each; every `data-money` element equals the mock's raw text; outgoing bodies contain no computed fields; no total in the DOM while editing; trailing zeros survive; GST rates 0/5/12/18/28, zero-rated and exempt; decimals (0.001, 1234567.891); credit notes, partial payment, overpayment; financial-year boundary 31-03/01-04; offline: three drafts → exactly three documents. axe, 44 pt, keyboard and screenshots saved.

## Done means
- [ ] Every kind has its new screens and states; matrix complete.
- [ ] All preserved behaviours proven by tests or marked `NOT RUN`.
- [ ] Route-specific document visuals preserve complete record/source data in DOM and still/no-WebGL modes.
- [ ] No money maths; scan passes.
- [ ] `STATUS.md` updated per batch.
