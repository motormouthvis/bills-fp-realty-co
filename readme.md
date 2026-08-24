# DN Staging Test

STAGING test realtor site for Neighborhood staging (v690): detector v7, ZIP-centroid fallback, and upgrade-request retire.

Public name: **DN Staging Test**. Public email: **wdmtaj@gmail.com**. GitHub repo name stays `bills-fp-realty-co`.

Identity decision note: [docs/site-identity.md](docs/site-identity.md).

## Public URL

- Site: https://dn-stagingtest.netlify.app
- Neighborhood embed: https://dn-stagingtest.netlify.app/neighborhoods

## Snippets (staging only)

Neighborhood `sdk.js` and `inline.js` stay on `staging.dreamneighborhood.com`. Do not use `app.dreamneighborhood.com`. Embedded School Explorer uses the staging Schools `embed.js` (Neighborhood `inline.js` only mounts `#dn-explorer`).

| Embed | Snippet |
| --- | --- |
| Popup Neighborhood Explorer | `https://staging.dreamneighborhood.com/explorer/sdk.js` |
| Embedded Neighborhood Explorer | `https://staging.dreamneighborhood.com/explorer/inline.js` (`#dn-explorer`; tabbed `/neighborhoods` sets `data-min-height="900"` so tab chrome + first screen fit without inner scroll; full variant uses `data-variant="full"`) |
| Popup School Explorer | Same staging Neighborhood SDK (`https://staging.dreamneighborhood.com/explorer/sdk.js`) |
| Embedded School Explorer | Staging Schools embed (`https://dream-schools-preview-b6b5fcaf4493.herokuapp.com/embed.js`) (`#dream-schools-explorer`; minimalist uses `data-variant="minimalist"`) |

Featured embeds on the site are only those four (nav: Neighborhood (T)/(F), Schools (T)/(M), plus the sitewide popup).

## Detector v7 pages

Labeled TEST / fake brokerage / not a real listing. Decision note: [docs/detector-v7-coverage.md](docs/detector-v7-coverage.md). Hub: [neighborhoods/detector-v7.html](neighborhoods/detector-v7.html).

- `/properties/4401-test-cedar-st-melbourne-fl.html` — street in URL, listing
- `/properties/test-listing-8841.html` — no street in URL, listing
- `/properties/3335-cunningham-rd-le-grand-ca.html` — Doherty-style street-file miss
- `/neighborhoods/hollywood-hills.html` — Hollywood Hills-style area (area name, not a street)
- `/neighborhoods/title-only-place.html` — title-only place name (`Los Feliz`)

## Local preview

```bash
npx --yes serve -l 4173 .
```
