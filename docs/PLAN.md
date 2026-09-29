# Plan

## Phase 0 — Discovery (in progress)
- [x] Research company online → COMPANY_PROFILE.md
- [x] Draft requirements and questions
- [ ] MD answers QUESTIONS.md → requirements v1.0 confirmed

## Phase 1 — Audit the vendor's `.wpress` file
- [ ] Receive file; extract (All-in-One WP Migration format) without running untrusted code
- [ ] Inventory: WP version, theme, plugins (licensing, abandoned, nulled/pirated), pages, media, DB content
- [ ] Security scan (malware, backdoors, hard-coded credentials, admin users)
- [ ] Run locally (Docker) and screenshot desktop + mobile
- [ ] Measure performance, accessibility, SEO
- [ ] Gap analysis vs confirmed requirements → AUDIT.md
- [ ] Recommendation: fix / partial reuse / rebuild

## Phase 2 — Build (depends on Phase 1 decision)
- [ ] Information architecture + wireframes for approval
- [ ] Design + content
- [ ] Development, product catalogue, forms
- [ ] Redirects from old Joomla URLs, SEO, analytics

## Phase 3 — Launch
- [ ] Staging review with MD, fixes
- [ ] Hosting, backups, security, DNS cutover (without breaking email)
- [ ] Handover guide for staff
