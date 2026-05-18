# Documentation project instructions

## About this project

- Customer-facing documentation site for **Mellanni Fine Linens**, built on [Mintlify](https://mintlify.com).
- Audience: shoppers and existing customers — not developers. Write for a general consumer.
- Pages are MDX files with YAML frontmatter. Configuration lives in `docs.json`.
- Site styling overrides live in `custom.css` (Mintlify auto-loads this filename — do not rename it).
- Run `mint dev` to preview locally. Run `mint broken-links` and `mint validate` before considering work done.

## Localization (critical)

- The site ships three locales via `navigation.languages` in `docs.json`: `en` (source of truth), `es`, `fr-CA`.
- English at the repo root is canonical. `es/` and `fr-CA/` mirror the EN tree **path-for-path**.
- When you add, rename, move, or delete an EN page: make the identical change in `es/` and `fr-CA/` (translated), and update all three `navigation.languages` groups in `docs.json`.
- Never let locale page sets diverge structurally from EN. A locale file with no EN counterpart, or an EN page with no locale counterpart, is a bug.
- In translations, translate prose, headings, frontmatter `title`/`description`, callout/table/link text. Never translate: frontmatter keys, MDX/JSX component names and props, `className`, code blocks, URLs, file/image paths, the brand name "Mellanni".

## Terminology

- Brand: **Mellanni** or **Mellanni Fine Linens** (never "Melani", "Mellani"). Never translate or pluralize the brand.
- Product categories: **sheet sets**, **pillowcases**, **duvet cover sets**.
- Flagship line: **Microfiber 1800 Series**, made of **double-brushed 100% microfiber**. Second material option: **Egyptian cotton**.
- Warranty: **Lifetime Satisfaction Money-Back Guarantee** (use this exact name; do not shorten to "warranty" in body copy).
- Sizes: Twin, Twin XL, Full, Queen, King, California King, Split King (sheets); Standard, Queen, King (pillowcases). Use these exact size names.
- Retail channels: mellanni.com, Amazon, Walmart, eBay, Wayfair.

## Style preferences

- Active voice, second person ("you"). Speak to the shopper.
- One idea per sentence. Concise. No marketing superlatives beyond verifiable claims (e.g. the Good Housekeeping "Best Sheets" recognition and review counts are factual and may be cited).
- Sentence case for headings and card/code titles.
- Bold for on-page UI and key claims; code formatting for file names, paths, commands.
- Internal links: root-relative, no extension (`/ordering/how-to-order`). External links: full URLs.

## Content boundaries

- Document only customer-facing topics: products, sizing, care, ordering, shipping, returns, warranty, business/wholesale, trust/sources.
- Do not document internal operations, supplier data, pricing strategy, or Amazon/marketplace seller-account internals.
- Keep factual claims (award years, review counts, guarantee terms) consistent across every page and locale. If a claim changes, grep all locales and update together.
