# HomeNex — Product Site

Marketing / landing site for **HomeNex**, the AI-powered CRM for Indian real estate agents.

> Every property lead answered in 30 seconds over WhatsApp — AI lead scoring, site-visit
> scheduling, property matching, commission tracking with GST invoicing, and festive greetings.

**Live product:** https://homenex.aiknol.com/ &nbsp;·&nbsp; **Product of** Apprend Technologies

## What's here

| Path | Purpose |
|------|---------|
| `index.html` | Single-page marketing site (hero, problem, features, how-it-works, pricing, footer). All CSS/JS inline — no build step. |
| `demo/index.html` | Placeholder "coming soon" page for the interactive demo. Replace with the real demo when built. |
| `_redirects` | Cloudflare Pages rule mapping `/demo` → `/demo/`. |

## Tech

- Plain static HTML + inline CSS + vanilla JS. **No framework, no build.**
- Fonts: Bricolage Grotesque (display) + Manrope (body) via Google Fonts.
- Theme: HomeNex forest green `#166534` on a warm off-white canvas, WhatsApp green `#25D366` accent.
- Fully mobile-responsive, scroll-reveal animations, animated WhatsApp chat mockup in the hero.
- Respects `prefers-reduced-motion` and `prefers-color-scheme` where relevant.

## Local preview

It's static — open `index.html` directly, or:

```bash
npx serve .        # or: python3 -m http.server 8080
```

## Deploy — Cloudflare Pages

This repo is set up to deploy as a Cloudflare Pages project (same pattern as the Apprend demo sites).

**One-time connection (Cloudflare dashboard):**
1. Pages → *Create a project* → *Connect to Git* → pick this repo.
2. Framework preset: **None**. Build command: *(empty)*. Build output directory: **`/`** (root).
3. Deploy. Every push to `main` auto-publishes.

The site is fully static, so no build step runs — Cloudflare just serves the files.
`_redirects` is picked up automatically.

## Updating the demo link

The hero, demo band, and footer link to `/demo` (currently the placeholder). When the real
interactive demo is ready, either replace `demo/index.html` or repoint those `/demo` links to
the new demo URL.
