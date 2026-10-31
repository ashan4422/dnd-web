# Open Questions for the Managing Director

Status legend: ❓ open · ✅ answered · 🟡 partly answered · ⏳ you'll provide later

## A. Company facts (to fix conflicting public data)
1. ⏳ Correct legal name — "Dee & Dee **Lanka** (Pvt) Ltd"? (brief said "Lank")
2. ⏳ Founding year (1990 vs 1982) and year incorporated (2005 vs 2012)?
3. ⏳ Head office: 281 Panchikawatte Rd, or 247 Sri Sangaraja Mawatha — or both (office + warehouse)?
4. ⏳ Full list of branches with address, phone, WhatsApp, email, hours, map pin (Kurunegala and Anuradhapura missing).
5. ⏳ Official email address(es) for enquiries.
6. ⏳ Stock range today (18,000+?) and which brands are officially authorized vs just stocked (NOK, Corteco, Nactec, LK, SKF, FAG, NSK, Koyo, Nachi, Asahi…?).
7. ⏳ Management / team members to show on the site (names, titles, photos)?

## B. The vendor's work
8. ✅ **(2026-10-31)** Design and content. We'll make a new design. You told the vendor content would be added by hand later through the admin panel. — What specifically were you unhappy with (design, content, speed, functionality, mobile, missed deadlines…)?
9. ❓ (not shared yet) What was the original brief/quotation given to them? Please share it if possible.
10. ❓ Is the vendor's site live anywhere (staging URL)? Do you still have hosting/domain/admin logins?
11. ✅ **(2026-10-31)** Rebuild on a better framework that's easier to change with Claude Code. The vendor's site is not being kept. — Do you want to (a) fix and finish their WordPress site, (b) reuse only content/assets, or (c) rebuild from scratch? My default is to decide after reviewing the file.

## C. Goals and audience
12. ✅ **(2026-10-31)** Mainly an **SEO tool** for Google rankings. Maybe an e-shop inside it later, but that is not the main site. — Main purpose: brand credibility, enquiries/quotes, online sales, or a searchable parts catalogue?
13. ✅ **(2026-10-31)** Everyone who uses the products: businesses, factories, car owners, machinery users, etc. — Main customers: workshops, retail mechanics, factories/industrial plants, government tenders, re-sellers, overseas buyers?
14. ✅ **(2026-10-31)** Not for now. Planned for the future. — Should prices or stock availability be shown? Any online ordering or payment?
15. ❓ (future, tied to the e-shop) Do you have a product/stock database (ERP/Excel) that could feed a catalogue, and how many items should be online?
16. 🟡 **(2026-10-31)** To be planned. — Languages: English only, or Sinhala / Tamil too?
17. ❓ Websites you like (competitors or others) and ones you dislike?

## D. Brand and content
18. ⏳ Logo files (vector), brand colours, fonts, brand guide?
19. ⏳ Photos: branches, warehouse, team, products — existing or need a shoot?
20. ⏳ Catalogues / brochures / certificates / distributor letters to publish?

## E. Technical and operations
21. 🟡 **(2026-10-31)** You will host it yourselves. Server type still open (see R1). — Who hosts the domain dndlanka.com and the current Joomla site? Keep the same host?
22. ❓ Who will update the site after launch, and how technical are they?
23. ❓ Email — should company email (Google Workspace / Microsoft 365 / host) be touched? (It must not break during migration.)
24. ✅ **(2026-10-31)** Not an issue. Development happens here with Claude Code. — Budget and target launch date?
25. ❓ How will you send the `.wpress` file (size?) — should it be committed to this private repo, or kept out of git?

---

# Round 2: questions for the planning phase (asked 2026-10-31)

R1. ✅ **(2026-10-31) VPS / cloud server.** — **Server type** for self-hosting: a VPS or cloud server that can run Node.js + PostgreSQL, or shared cPanel/PHP hosting only? **This decides the framework** (see TECH_STACK.md).
R2. 🟡 **(2026-10-31) MD asked for a plainer explanation first** (added to TECH_STACK.md). — Do you approve the recommended stack (**Next.js + Payload CMS + PostgreSQL**)?
R3. ✅ **(2026-10-31) Quick reference only.** Unpack safely and salvage useful structure, images and text. No full audit. — What to do with the vendor's `.wpress` file now that we are rebuilding: use it as a quick reference (structure, images, anything worth keeping), or skip it?
R4. ✅ **(2026-10-31) A page per part number.** Bulk import from Excel/ERP needed. Item count at launch still open. — How detailed should the catalogue be? Separate SEO pages per part number (e.g. "6205-2RS bearing") or category/brand pages only? Roughly how many items at launch?
R5. ❓ Who will use the admin panel (how many people, which roles: admin / editor / branch staff)?
R6. ❓ Keep the domain **dndlanka.com** and redirect the old Joomla URLs (`/index.php/...`) so existing Google rankings carry over?
R7. ❓ Build multi-language support in from day one (English first; Sinhala/Tamil can be added later without a rebuild)?
R8. ❓ Add a blog/knowledge section (guides, maintenance tips, news) for SEO?
R9. ❓ Where should enquiries go: email, WhatsApp per branch, stored in the admin panel, or all three?
R10. ❓ Do you have Google Business Profiles for each branch, Google Search Console and Google Analytics? Who owns the logins?
R11. ❓ Who hosts the company email today? DNS changes at launch must not break it.
R12. ❓ May I copy the existing text from the current Joomla site (about, vision/mission, product descriptions) as starter content to edit later?
R13. ❓ Design direction: any reference websites you like? Keep the current logo and colours, or rebrand?
