# Generational Wealth

Marketing site for **Generational Wealth** — a private, disciplined swing & scalp trading community.
Live brand: [gwhlds.com](https://gwhlds.com) · IG: [@genwealthtrade](https://www.instagram.com/genwealthtrade)

Static site, no build step. Just HTML, inline CSS, vanilla JS, and the logo.

## Files

| File | Purpose |
|------|---------|
| `index.html` | The landing page (hero, method, what's inside, results, join, FAQ) |
| `terms.html` | Terms of Service & risk disclaimer |
| `privacy.html` | Privacy policy |
| `assets/logo.png` | Brand logo (gold & green GW shield) |

## Brand system

- **Colors:** navy `#070B17` / `#0F172A`, gold `#D4AF37`, green `#22C55E`, cream `#FBF7EA`
- **Type:** Inter (body), Playfair Display (italic display), JetBrains Mono (labels)
- **Voice:** *process over hype · discipline before entries · capital preservation first*

## Local preview

Open `index.html` directly in a browser, or serve the folder:

```bash
npx serve .
```

## Things to wire up before launch

These are intentionally left as placeholders — search and replace:

1. **Patreon URL** — every "Join on Patreon" button currently points to `https://www.patreon.com/`. Replace with the real Generational Wealth Patreon page (search `patreon.com/` in `index.html`).
2. **Results screenshots** — the three cards in the `#results` section are styled placeholders (`▒▒▒`). Swap each `.shot` figure for a real member screenshot `<img>`.
3. **Domain** — canonical/OG URLs use `https://gwhlds.com/`. Update if the domain changes.
4. **Legal review** — `terms.html` and `privacy.html` are solid boilerplate for an educational trading community, but have them reviewed by counsel before relying on them.

## Deploy to Vercel

Pure static site — Vercel needs no configuration.

1. Push to `ArasPasha/GenerationalWealth`.
2. Go to [vercel.com/new](https://vercel.com/new) and import the repo.
3. Framework Preset: **Other** · Build Command: *(empty)* · Output Directory: *(empty — serves repo root)*.
4. Deploy. Every push to `main` auto-deploys; pull requests get preview URLs.
5. Add the custom domain (`gwhlds.com`) under the project's **Domains** settings.
