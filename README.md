# Zesencia Website

The public website for Zesencia Technologies — built with [Astro](https://astro.build) and deployed to [Cloudflare Pages](https://pages.cloudflare.com).

## Site Map

- `/` — Home
- `/about` — About
- `/products` — Products
- `/contact` — Contact
- `/privacy` — Privacy Policy
- `/terms` — Terms of Use

## Tech Stack

- [Astro](https://astro.build) — static site generation, zero client-side JS by default
- Plain CSS (custom properties, no framework/utility library)
- TypeScript (strict mode)
- Hosted on Cloudflare Pages, deployed automatically on push via Cloudflare's Git integration

## Getting Started

Requires Node.js 20+.

```bash
npm install
npm run dev
```

The site will be available at `http://localhost:4321`.

## Commands

| Command           | Action                                             |
| ------------------ | --------------------------------------------------- |
| `npm install`       | Install dependencies                                 |
| `npm run dev`       | Start the local dev server                           |
| `npm run build`     | Type-check (`astro check`) and build to `./dist/`    |
| `npm run preview`   | Preview the production build locally                 |

## Deployment

This repo is connected to a Cloudflare Pages project. Every push to `main` triggers a new deployment automatically.

Cloudflare Pages build settings:

- **Build command:** `npm run build`
- **Build output directory:** `dist`

No environment variables or adapters are required — the site builds fully static.

## Project Structure

```
src/
├── components/     # Shared UI (nav, footer)
├── layouts/        # Layout.astro — shared <head>, nav, footer wrapper
├── pages/          # One file per route
└── styles/         # global.css — design tokens and shared styles
public/             # Static assets (favicon, etc.)
```

## Content Notes

- Legal copy (`/privacy`, `/terms`) is a starting point suitable for Apple's App Store review requirements. Update it as products, data collection, and third-party services are added.
- `/products` currently shows a "Coming Soon" placeholder. When apps ship, give each one its own section with screenshots, description, and an App Store link.
