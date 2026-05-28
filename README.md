# Peak Money — UX Forensics · Chapter II

> The Quick Actions Problem — a focused analysis of why fintech dashboards need fewer primary actions, cross-checked against 10 banking references from Mobbin and the cognitive psychology canon.

![Status](https://img.shields.io/badge/status-published-success)
![Type](https://img.shields.io/badge/type-static%20site-blue)
![Build](https://img.shields.io/badge/build-none-lightgrey)
![License](https://img.shields.io/badge/license-MIT-green)

---

## Overview

Single-page editorial report. Self-contained `index.html` with embedded CSS and JavaScript. Zero build step, zero dependencies beyond Google Fonts (loaded at runtime).

The report covers:

- The cognitive case for fewer focal points (Miller, Hick, Von Restorff, Nielsen H8, Pareto, Occam)
- A calibrated matrix of ideal counts per element category
- Direct evidence from 10 banking apps indexed in Mobbin
- Field verification across Robinhood, Wealthfront, Cash App, Chase, Revolut
- The verdict and recommended configuration for Peak Money

---

## Project structure

```
peak-money-chapter-ii/
├── index.html        # The full report — self-contained
├── vercel.json       # Static deployment config (no build)
├── README.md         # You are here
├── LICENSE           # MIT
└── .gitignore        # Standard ignores
```

No `package.json`. No `node_modules`. No bundler. The site is pure HTML/CSS/JS served as-is.

---

## Deploy

### Option 1 — Vercel via GitHub (recommended)

1. Push this repository to GitHub
2. Go to [vercel.com/new](https://vercel.com/new)
3. Click **Import** next to your repository
4. Leave all framework presets blank. Vercel will detect a static site from `vercel.json`
5. Click **Deploy**

Vercel will assign a URL like `your-repo.vercel.app`. Push to `main` to redeploy automatically.

### Option 2 — Vercel CLI

```bash
npm i -g vercel
cd peak-money-chapter-ii
vercel
```

Follow the prompts. Accept the defaults. No build command, no output directory needed.

### Option 3 — Drag & drop

1. Go to [vercel.com/new](https://vercel.com/new)
2. Drag the **entire folder** into the drop zone (not just the HTML file)
3. Click **Deploy**

### Option 4 — Any static host

This is plain HTML — it deploys identically to Netlify, Cloudflare Pages, GitHub Pages, S3, or any web server. No special configuration required outside `vercel.json` (which is ignored by non-Vercel hosts).

---

## Local development

No server required. Open the file directly:

```bash
open index.html
```

Or run a quick local server if you prefer:

```bash
# Python
python3 -m http.server 8000

# Node
npx serve .
```

Then visit `http://localhost:8000`.

---

## Tech stack

- HTML5 (single file)
- CSS3 with variables and `@font-face` via Google Fonts
- Vanilla JavaScript (IntersectionObserver for scroll reveals)
- Google Fonts: Fraunces (variable serif), Geist (sans), JetBrains Mono

No frameworks. No build tools. Total weight on the wire: roughly 48 KB of HTML plus the Google Fonts payload.

---

## Browser support

Tested on current versions of Chrome, Safari, Firefox, and Edge. Uses modern features (CSS variables, IntersectionObserver, variable fonts) — fine on anything from 2020 onward.

---

## Related

- **Chapter I — The Dashboard Audit** → [peak-money-ux-insights-v1.vercel.app](https://peak-money-ux-insights-v1.vercel.app)

---

## License

MIT — see `LICENSE`.
