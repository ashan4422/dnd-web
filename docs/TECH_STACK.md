# Technology Stack: Options & Recommendation

Status: **Recommendation, waiting for MD approval (R1, R2).** 2026-10-31.

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
