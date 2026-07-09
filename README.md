# Flowerenco 🌸

A tiny one-person ceramic studio storefront — whimsical, hand-painted **character & portrait bud vases**
made to order from a photo of a person or pet. Live at **[flowerenco.com](https://www.flowerenco.com)**.

Built as a **Wix Headless** site with **Astro** (Wix-managed hosting).

## What's inside

- **Storefront** (Wix Stores / eCommerce) — three custom vase products (Portrait / Pet / Duo), each in
  **Small / Medium / Large**.
- **Custom order flow** (per product): pick a **size** → pick a **style** (Matte Folk / Glossy Doodle /
  Blue Willow) → **upload a reference photo** → **add notes** → add to basket → card checkout. The size,
  style, notes and photo travel with the order (buyer note).
- **Carousel gallery** of subject-matched style examples on each product page.
- **Gallery** (Wix Portfolio) — a showcase of past commissions.
- **Say Hi** (Wix Forms) — an inquiry form; submissions also land in a **Studio Messages** CMS collection.
- **Basket** — per-item cards with the uploaded photo, "Change product" (re-opens pre-filled) and "Delete".
- **Thank-you page** — shows the real order number (looked up via a backend API route).

## Tech

- [Astro](https://astro.build) + [`@wix/astro`](https://dev.wix.com/docs/go-headless) (managed headless)
- Wix SDK: `@wix/stores`, `@wix/ecom`, `@wix/redirects`, `@wix/portfolio`, `@wix/forms`, `@wix/data`,
  `@wix/media`, `@wix/sdk`, `@wix/essentials`
- React islands only where interactivity is needed (order widget, basket, contact form)

## Develop

```bash
npm install --ignore-scripts
npm run dev       # local dev server (wix dev)
npm run build     # wix build
npm run release   # publish to Wix hosting
```

> Requires a logged-in Wix CLI session and the project's `.env.local` (not committed).
> `wix.config.json` holds the public `siteId` + OAuth `appId` (client id).
