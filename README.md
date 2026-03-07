# Zest — Landing Page

Marketing landing page for [Zest](https://tryzest.app), the AI prompt optimizer. Single-file static site — no framework, no build step. Hosted on GitHub Pages (or any static host).

## What it does

Presents Zest to potential users with:

- Hero section with tagline and CTA
- Before/after prompt comparison demo
- Theme showcase (5 built-in themes)
- Pricing section with Free vs Pro toggle (monthly/annual)
- Download buttons (macOS + Windows) with waitlist fallback
- Footer with links

## Project structure

```
zest-web/
├── index.html              # Full landing page (HTML + CSS + JS, single file)
└── upgrade/
    └── success.html        # Post-checkout success page
```

## Development

No build step. Just open `index.html` in a browser:

```bash
open index.html
```

Or serve locally:

```bash
python3 -m http.server 8000
```

## Deployment

Any static hosting works. The site is a single HTML file with inline CSS and JS.

**GitHub Pages:**
```bash
# Push to main, enable Pages in repo settings (source: main branch, root)
git push
```

**Custom domain:** Point `tryzest.app` DNS to GitHub Pages and add a `CNAME` file.

## Related repos

- [`zest`](https://github.com/bugfreev587/zest) — Desktop app (Wails v2)
- [`zest-backend`](https://github.com/bugfreev587/zest-backend) — Server API (Go + Gin)
