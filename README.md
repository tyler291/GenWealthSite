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

1. ~~**Patreon URL**~~ ✅ Done — all "Join on Patreon" buttons + the footer icon point to `https://www.patreon.com/cw/Generational_Wealth`.
2. **Results screenshots** — the three cards in the `#results` section are styled placeholders (`▒▒▒`). Swap each `.shot` figure for a real member screenshot `<img>`.
3. **Testimonials** — sample placeholders in the `GW_TESTIMONIALS` array (in `index.html`). Replace quotes/authors with real ones.
4. **Instagram feed** — set `BEHOLD_FEED_ID` in the `#instagram` script to your Behold JSON feed ID to pull real posts (free at app.behold.so). Empty = placeholder cards.
5. **Domain** — canonical/OG/sitemap URLs use `https://gwhlds.com/`. Update if the domain changes.
6. **Legal placeholders** — in `terms.html`, replace `[GOVERNING-LAW STATE]` (appears twice) with your jurisdiction and insert your registered legal entity name; in `privacy.html`, add a privacy contact email. Both pages are drafted to be highly protective but **must be reviewed by a licensed attorney** before you rely on them.
7. **Google Search Console** — uncomment the `google-site-verification` meta in `index.html` and paste your token to verify the domain.

## SEO

- `index.html` has full meta (title/description/keywords), Open Graph + Twitter cards, and JSON-LD for **Organization + WebSite + FAQPage** (the FAQ is eligible for rich results — keep the schema in sync with the on-page FAQ).
- `robots.txt` and `sitemap.xml` are at the site root (update the domain inside them if it changes).

## Deploy to Vercel

Pure static site — Vercel needs no configuration.

1. Push to `ArasPasha/GenerationalWealth`.
2. Go to [vercel.com/new](https://vercel.com/new) and import the repo.
3. Framework Preset: **Other** · Build Command: *(empty)* · Output Directory: *(empty — serves repo root)*.
4. Deploy. Every push to `main` auto-deploys; pull requests get preview URLs.
5. Add the custom domain (`gwhlds.com`) under the project's **Domains** settings.
