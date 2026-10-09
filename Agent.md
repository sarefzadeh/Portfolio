# Agent.md — Portfolio Site

Guide for any AI assistant working on this project. Read fully before making changes.

## Project
Personal portfolio for a Product Designer. Goal: a hiring manager understands the owner's value (zero-to-one products + case studies) in under a minute.

- Main working file: `Portfolio Site.dc.html` (single-file site: home, 3 product pages, 5 case studies, articles list + article pages).
- Offline export: `Saeid Arefzadeh - Portfolio Site.html` — generated from the main file; never edit it directly, regenerate it.
- Assets: `assets/` (favicon, product images). `support.js` is runtime — do not edit.
- Older files (`Portfolio v2…v5`, `Redesign`, etc.) are archived iterations — don't touch unless asked.

## How the owner works
- Communicates in Persian; site content is in English. Reply in Persian unless asked otherwise.
- Wants short, direct answers. No long explanations, no filler.
- If something is ambiguous, ask briefly **before** acting. Offer choices with a sensible default.
- When asked a yes/no question ("can you…?"), answer yes/no first — don't start doing the work.
- Every change must be kept in sync with the GitHub repository.

## Red lines (never do)
1. **Never change what wasn't asked.** Small request = small, targeted edit. Suggest broader improvements; don't apply them.
2. **No dark mode.** It was removed intentionally.
3. **No Persian/RTL version on the site** for now (strings may stay in source for later).
4. **No yellow text.** Yellows are for backgrounds only.
5. **No invented colors** outside the palette below (exception: green status dot `#2E9E5E`).
6. **No fake/placeholder content** (fake names, numbers, "XX", lorem ipsum, fake stats). Leave a clear slot or ask.
7. **No personal/sensitive data** added anywhere without explicit approval.
8. **Don't break mobile.** Every change must be checked at ~320–390px and desktop.
9. No emoji, no heavy gradients, no decorative SVG illustrations.

## Design system
**Palette**
- Text (darkest): `#060B26`; secondary text = lighter shades of it (must stay ≥4.5:1 contrast).
- Primary / buttons / dark sections: `#0B1C40` with white text.
- Soft blue (selective use, hover/links/accents): `#265573`.
- Yellow `#F2DA91` + soft yellow tints (`#FBF4DC`, `#FDF8EA`) — backgrounds only.
- Tan/bronze `#BF8B5E` — small accents only (icons, dividers, badges, the "zero to shipped" highlight). Tan tint `#F8EEDF` for soft boxes.
- Page background: white. Cards/soft sections: one neutral light tint (`#EEF1F5` / `#F4F5F8`).

**Type:** Bricolage Grotesque (headings), Onest (body). Mobile body text must stay readable (no tiny text).

**Components & patterns**
- Sticky header with frosted-glass effect + subtle gray border/shadow. Order: Contact, Case studies, Products, Resume. Back button on inner pages.
- Contact = icon + text on desktop, icon only on mobile (≤640px).
- Contact modal: email, phone, Telegram, LinkedIn; closes on Esc / click outside; soft bubble animation.
- "Built from zero" cards: order is icon+label → title → View project → image. Images aligned across cards.
- Favicon (`assets/favicon.png`) is also the header logo and the loading-screen icon (very slow, gentle heartbeat pulse, centered).

## Technical rules
- Inline styles only; media queries only in the head `<style>` block (via `data-*` attribute selectors).
- Keep layouts fluid (grid/flex + gap, `minmax(0,1fr)`); no fixed widths that break small screens.
- After editing, regenerate the offline export and sync to GitHub.

## Known open issues (backlog)
Resume link, placeholder content, empty image slots, Writing link in header, back-button behavior, focus handling in modal, contrast on small text, real reading times, real per-page URLs, social preview image.
