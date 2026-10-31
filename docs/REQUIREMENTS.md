# Requirements

Status: **v0.2, 2026-10-31.** Updated with the MD's round-1 answers. Items still waiting on the round-2 questions in [QUESTIONS.md](QUESTIONS.md) are marked *Pending*.

## Confirmed direction
- **Rebuild from scratch** on a modern framework that is easy to change with Claude Code. The vendor's WordPress site is not being kept.
- **Main purpose: SEO.** Rank on Google for bearings, seals and related searches across Sri Lanka.
- **Audience:** anyone who uses the products: businesses, factories, workshops, car owners, machinery users.
- **New design**, to be planned. Brand assets come after the planning phase.
- **Content is entered by D&D staff through an admin panel.** So the admin panel must be easy to use.
- **Self-hosted** by D&D on a **VPS / cloud server**.
- **Future, not now:** e-shop, prices, stock availability, multiple languages. The architecture must allow all of these later without a rebuild.

## Business goals
- G1. Rank on page 1 of Google for product and brand searches in Sri Lanka (e.g. "bearings Sri Lanka", "oil seals Colombo", part-number searches).
- G2. Turn visitors into enquiries (call, WhatsApp, form, branch visit).
- G3. Help customers find the right part quickly (by category, brand, size or part number).
- G4. Send customers to the nearest of the 5 branches (local SEO).
- G5. Leave room for an e-shop later.

## Functional requirements
| ID | Requirement | Status |
|---|---|---|
| F1 | Pages: Home, About (history, vision/mission, management), Products, Brands, Industries, Branches, Contact | Confirmed (scope) |
| F2 | Admin panel where staff add and edit pages, products, categories, brands, industries, branches, images and SEO fields without a developer | **Confirmed** |
| F3 | Product catalogue: category → sub-category → **one page per part number**, with brand, specs and size tables | **Confirmed** (R4) |
| F3a | Bulk import/update of products from Excel/CSV (and later the ERP) | **Confirmed** (R4) |
| F4 | Search by keyword, part number or dimensions (ID × OD × width) | Proposed |
| F5 | Enquiry / request-a-quote form + WhatsApp click-to-chat per branch | Proposed; routing *Pending R9* |
| F6 | One page per branch: map, phone, WhatsApp, hours | Proposed |
| F7 | One page per brand and per industry (SEO landing pages) | Proposed |
| F8 | Blog / knowledge base | *Pending R8* |
| F9 | Downloadable catalogues (PDF) | Proposed |
| F10 | Redirect manager in the admin panel; 301 redirects from old Joomla URLs | Proposed; *Pending R6* |
| F11 | Multi-language-ready content model (English first; Sinhala/Tamil later) | Proposed; *Pending R7* |
| F12 | E-shop (cart, checkout, payments, stock) | **Future**. Keep the product model compatible |

## SEO requirements (core of the project; see [SEO_STRATEGY.md](SEO_STRATEGY.md))
- S1. Server-rendered or static HTML for every public page (no client-only rendering).
- S2. Editable SEO title, meta description, social image and canonical URL on every page and product.
- S3. Auto-generated `sitemap.xml` and `robots.txt`; hreflang tags once languages are added.
- S4. Structured data: Organization, LocalBusiness per branch, Product, BreadcrumbList, FAQ.
- S5. Core Web Vitals "Good" on mobile; Lighthouse ≥ 90 in all categories.
- S6. Clean, keyword-friendly URLs (`/products/bearings/deep-groove/6205-2rs`).
- S7. Image optimisation (WebP/AVIF, responsive sizes, alt text required in the admin panel).

## Non-functional
- Mobile-first and fast on Sri Lankan mobile networks.
- Current, supported software only. Automated backups, HTTPS, security headers.
- The whole site (content model included) is defined in code in this repo, so Claude Code can change it safely.
- Admin roles and permissions (*Pending R5*).
