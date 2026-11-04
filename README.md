# MAZZ.AI — Website Pages

Standalone HTML pages for MAZZ.AI, the AI call & chat assistant for restaurants. Each file is a self-contained page (its own `<style>`, no build step) designed in one consistent black-and-lime brand system.

## Pages

| Page | File | Live preview | Notes |
|---|---|---|---|
| Sign in | `sign-in.html` | [Preview](https://claude.ai/artifact/QFiP4bKHHb2rk9W1GaZERJ) | Restaurant owner login |
| Landing page | `landing.html` | [Preview](https://claude.ai/artifact/Td8khqVDiE8pBFFNqbMWEC) | Public marketing page, pricing teaser, Founding Partner callout |
| Home (dashboard) | `home.html` | [Preview](https://claude.ai/artifact/S5PFpbs1a8agBXeqvBEkYB) | Logged-in restaurant dashboard: pilot progress, call stats, quick actions |
| Blog | `blog.html` | [Preview](https://claude.ai/artifact/W2XFkmcUYRaQyhmCE6SGGu) | Featured article + post list |
| Pricing | `pricing.html` | [Preview](https://claude.ai/artifact/EEpL3wvcAgD8S9b3p3eY17) | Pilot offer, AI adoption roadmap, rate + interactive cost calculator, Founding Partner Program |
| FAQ | `faq.html` | [Preview](https://claude.ai/artifact/9NX5PvCtUNjpzrBTLKjZMT) | Accordion FAQ grouped by General / Pilot & pricing / Founding Partner / Technical |
| Terms & Conditions | `terms.html` | [Preview](https://claude.ai/artifact/D2uCkhnJ8uBy6V893bfqFi) | Legal terms with sticky table of contents |

## Opening the pages

No build step, no dependencies to install. Open any `.html` file directly in a browser, or serve the folder with any static file server:

```bash
npx serve .
```

## Brand system

Every page shares the same design tokens, defined at the top of its `<style>` block:

| Token | Value | Use |
|---|---|---|
| `--bg` | `#0a0a0a` | Page background |
| `--bg-card` / `--bg-raised` | `#131310` / `#111110` | Card and panel surfaces |
| `--line` | `#2a2a22` | Borders, dashed ticket-style dividers |
| `--ink` | `#f5f5f0` | Primary text |
| `--ink-dim` / `--ink-faint` | `#a2a298` / `#6b6b62` | Secondary / tertiary text |
| `--lime` | `#c6f135` | Brand accent — logo, CTAs, highlights |
| `--lime-soft` | `#e9ffa8` | Hover/active accent text |

**Typography**: [Archivo Black](https://fonts.google.com/specimen/Archivo+Black) for headings and the logo, [Inter](https://fonts.google.com/specimen/Inter) for body and UI text, [Space Mono](https://fonts.google.com/specimen/Space+Mono) for data, labels, and receipt-style numbers. Loaded from Google Fonts.

**Logo**: the wordmark is always two tones — `MAZZ` in white (`#ffffff`), `.AI` in lime (`var(--lime)`) — matching the source logo.

**Motif**: two diagonal lime glow beams anchor opposite corners on every page (echoing the logo), and cards/receipts use a dashed "order ticket" tear-line style, reflecting the restaurant/POS subject matter.

## Key facts baked into the copy

Keep these consistent if content changes — they're repeated across multiple pages:

- **3-month free pilot** for every new restaurant.
- **AI adoption roadmap**: Month 1 = 25% AI / 75% human, Month 2 = 50/50, Month 3 = 75% AI / 25% human, after pilot = 100% AI (human handoff always available).
- **Pricing**: 6 EGP / minute after the pilot, first 1,000 minutes/month free for life, no maximum usage limit.
- **Founding Partner Program**: first 3 restaurants only — 12 months of maintenance & support, free feature development (only a resulting per-minute cost increase is billed), priority on future features.
- **Custom and special-request orders are handled by the AI directly**, not escalated to a human — only complaints and genuinely ambiguous situations route to staff.

## Editing

Each page is fully self-contained (CSS inlined, no shared stylesheet file), so a change to the brand tokens needs to be applied per file. If you add a page, copy the `:root` token block and nav/footer markup from `landing.html` as the starting point for consistency.
