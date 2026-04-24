# fluera-engine-landing

Marketing site for the **Fluera Engine** Flutter SDK — live at
[engine.fluera.dev](https://engine.fluera.dev).

Built with Astro 5 + Tailwind 3, deployed to GitHub Pages via Actions.

## Develop

```bash
npm install
npm run dev        # http://localhost:4321
```

## Build

```bash
npm run build      # outputs to dist/
npm run preview    # serves the built site locally
```

## Deploy

Push to `main`. The workflow in `.github/workflows/deploy.yml` builds and
publishes to GitHub Pages. The custom domain `engine.fluera.dev` is configured
via `public/CNAME`.

DNS: a `CNAME` record on `engine` → `lorencoshametaj.github.io` at the
registrar (Porkbun).

## Structure

```
src/
├── components/   # Nav, Footer, Head, PageHero, FeatureCard
├── layouts/      # BaseLayout
├── lib/site.ts   # SITE config (name, url, links)
├── pages/        # index · quickstart · pricing
└── styles/       # global.css (Tailwind + design tokens)
```

## Content

- `index.astro` — landing (hero, stats, capabilities, core-vs-pro, CTA)
- `quickstart.astro` — 5-minute integration guide
- `pricing.astro` — Core (open) vs Pro (commercial) + FAQ

Design tokens, color palette (`ink`/`paper`/`accent`) and utility classes
(`.btn-primary`, `.eyebrow`, `.prose-v2`, …) match the consumer site
`fluera.dev` for brand consistency.
