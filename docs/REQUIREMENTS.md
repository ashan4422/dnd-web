# Requirements — DRAFT (not yet confirmed by the MD)

Status: **Draft v0.1 — 2026-09-29.** Built from research only. Each item becomes "Confirmed" once answered in [QUESTIONS.md](QUESTIONS.md).

## Business goals (assumed)
- G1. Present D&D Lanka as Sri Lanka's leading, trusted bearings & sealing specialist (35+ years).
- G2. Generate trade enquiries / quote requests from workshops, fleet operators, factories and resellers.
- G3. Help customers find the right part quickly (by category, brand, size / part number).
- G4. Direct customers to the nearest of the 5 branches.
- G5. Showcase the brands carried and any authorized distributorships.

## Functional requirements (proposed)
| ID | Requirement | Status |
|---|---|---|
| F1 | Home, About (history, vision/mission, management), Products, Brands, Industries, Branches, Contact | Proposed |
| F2 | Product catalogue by category → sub-category → brand, with specs/size tables | Proposed — scope TBD |
| F3 | Search by part number / dimensions (ID × OD × width) | Proposed — depends on stock data |
| F4 | Enquiry / request-a-quote form (and WhatsApp click-to-chat) | Proposed |
| F5 | Branch pages with map, phone, hours | Proposed |
| F6 | Brands page with logos and distributorship status | Proposed |
| F7 | Downloadable catalogues/brochures (PDF) | Proposed |
| F8 | Staff can edit content, products, branches without a developer | Proposed |
| F9 | Online ordering / prices / e-commerce | **Unknown** |
| F10 | Languages: English; Sinhala / Tamil? | **Unknown** |

## Non-functional (proposed)
- Mobile-first, fast on Sri Lankan mobile networks (target Lighthouse ≥ 90).
- Current, supported software (PHP 8.2+, latest WordPress if we keep WordPress), HTTPS, backups, security hardening.
- SEO: clean URLs, 301 redirects from old `/index.php/...` URLs, Google Business Profiles for all branches, schema.org LocalBusiness.
- Consistent branding (logo, colours) — assets to be supplied.
