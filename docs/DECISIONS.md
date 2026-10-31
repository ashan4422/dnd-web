# Decisions Log

| Date | Decision | Reason | Status |
|---|---|---|---|
| 2026-09-29 | Keep all planning/progress in separate `.md` files under `docs/` | MD's instruction | Final |
| 2026-09-29 | Do not run the vendor's code until it has been scanned | Unknown third-party code may contain malware or nulled plugins | Final |
| 2026-10-31 | **Rebuild from scratch**; do not continue the vendor's WordPress site | MD: unhappy with design; wants a framework that's easier to change with Claude Code | Final |
| 2026-10-31 | Main objective of the site is **SEO / Google ranking** | MD | Final |
| 2026-10-31 | E-shop, prices, stock and extra languages are **future phases**, but the architecture must support them | MD | Final |
| 2026-10-31 | Self-hosted by D&D | MD | Final |
| 2026-10-31 | Content entered by D&D staff through an admin panel | MD | Final |
| 2026-10-31 | Stack: **Next.js + Payload CMS + PostgreSQL** (fallback Laravel + Filament if PHP-only hosting) | See TECH_STACK.md | **Proposed: waiting for MD (R1, R2)** |
| 2026-10-31 | Hosting on a **VPS / cloud server** (Node.js + PostgreSQL capable) | MD (R1) | Final |
| 2026-10-31 | `.wpress` file: **quick reference / salvage only**, no full audit | MD (R3) | Final |
| 2026-10-31 | Catalogue: **one SEO page per part number**, with bulk import from Excel/ERP | MD (R4); biggest long-tail SEO opportunity | Final |
