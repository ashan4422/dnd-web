# Technology Stack: Options & Recommendation

Status: **Recommendation.** Hosting confirmed as a **VPS** (R1). Waiting for MD approval of the framework (R2). 2026-10-31.

## What the stack must do
1. Be excellent for SEO (server-rendered/static pages, full control of meta tags, schema and URLs).
2. Give non-technical staff an easy admin panel.
3. Keep everything as code in this repo, so Claude Code can add fields, pages and features safely.
4. Support multiple languages and an e-shop later without a rebuild.
5. Be self-hostable by D&D.

## Options compared
| | **A. Next.js + Payload CMS** (recommended) | B. Laravel + Filament | C. Astro + Git-based CMS (Keystatic/Decap) | D. WordPress (vendor's approach) |
|---|---|---|---|---|
| Language | TypeScript, one codebase | PHP | TypeScript | PHP + plugins |
| Admin panel | Built-in, generated from code-defined collections | Very good, built in code | Basic; edits are git commits | Familiar, but configured by clicking |
| Easy to change with Claude Code | ★★★★★: content model, admin and site all in typed code | ★★★★ | ★★★★ | ★★: logic spread across plugins and database |
| SEO | ★★★★★: SSR/static, official SEO, redirects and form-builder plugins | ★★★★ | ★★★★★ | ★★★★ (with plugins) |
| Large catalogue (thousands of items) | ★★★★★ (PostgreSQL) | ★★★★★ | ★★: not suited | ★★★ |
| Languages later | Built-in field-level localisation | Packages | Manual | Paid plugins |
| E-shop later | Official e-commerce plugin (beta in 2026; fine because the shop is a later phase) | Lunar / Bagisto packages | Not suited | WooCommerce |
| Hosting needs | VPS that runs Node.js + PostgreSQL (≈2 GB RAM) | Works on PHP hosting or a VPS | Static hosting, the cheapest | PHP hosting |
| Security upkeep | Low: small dependency set | Low | Lowest | High: plugin updates, a common attack target |

## Recommendation: Option A, Next.js + Payload CMS 3 + PostgreSQL
- Payload's admin panel is generated from collections we define in TypeScript. Adding "a Brand logo field" or "a new Industries page type" is a small code change Claude Code can make and review.
- The website (Next.js) and the admin panel live in **one app, one repo, one deployment**.
- Official plugins cover SEO fields, redirects, form builder, nested categories and search, so less custom code.
- Localisation is built in: we enable it from day one with English only, and Sinhala/Tamil become a config change plus translations.
- The e-commerce plugin adds products/variants, carts, orders and payments later, on the same product data.
- Self-hosting: Docker image + PostgreSQL on a VPS (e.g. DigitalOcean, AWS Lightsail, Hetzner or a Sri Lankan VPS provider), with Nginx/Caddy for HTTPS.

**Fallback:** if D&D's hosting can only run PHP (shared cPanel), choose **Option B (Laravel + Filament)**.

## Proposed details (if A is approved)
- Payload 3.x (latest stable), Next.js (version supported by Payload), TypeScript, Tailwind CSS
- PostgreSQL 16+; media stored on local disk or S3-compatible storage
- Docker Compose for local development and production
- GitHub Actions: lint, typecheck, tests, Lighthouse CI on every PR
- Versions pinned at setup, after checking the npm and GitHub release pages

---

## In plain words (for the MD)

**What the three parts are**
| Part | What it does | Everyday comparison |
|---|---|---|
| **Next.js** | Builds the public website that customers and Google see | The shop front |
| **Payload CMS** | The admin panel where staff log in to add products, photos, branches and text | The back office |
| **PostgreSQL** | The database that stores all products, pages and enquiries | The stock ledger |

All three run together as **one app on your VPS**. Staff never touch code; they use the admin panel in a web browser, much like WordPress's dashboard.

**Why it's better for you than WordPress**
1. **Changes are quick and safe with Claude Code.** In WordPress, much of the site lives in plugins and settings clicked together in the dashboard, which is hard to change reliably. Here, everything is written as code in this repository. If you say "add a *Max RPM* field to bearings", Claude Code edits a few lines, the admin panel shows the new field automatically, and the change is reviewed and tracked in git (you can always undo it).
2. **Better for Google.** Pages are delivered as ready-made HTML and load very fast, and Google rewards speed. We control every title, description, URL and structured-data tag.
3. **Built for thousands of parts.** You chose a page per part number. We can bulk-import from Excel/your ERP, and each part gets its own fast page.
4. **Ready for the future without a rebuild.** Sinhala/Tamil and the e-shop are built-in features we switch on later, using the same product data.
5. **Fewer security problems.** No pile of third-party plugins to keep updated, so less exposure to the attacks WordPress sites commonly suffer.

**Honest drawbacks**
- It needs a **VPS** (which you have chosen), not cheap shared hosting. A suitable server is typically around USD 10–25/month (check current prices with your provider).
- Fewer freelancers know Payload than WordPress. Since development is done here with Claude Code, that matters less, and it is standard TypeScript/React that many developers know.
- Payload's e-shop add-on is still maturing. It is a future phase, so it will have matured by the time we need it; if not, we can add a proven e-commerce engine alongside.

**What day-to-day use looks like**
- Staff log in at `dndlanka.com/admin`, then click *Products → Add new*, fill in the name, brand, sizes and photos, set the SEO title, and press *Publish*. The page is live straight away.
- For bulk changes (e.g. 2,000 new oil seals), send an Excel file and we import it.
