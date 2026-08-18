# DN Staging Test

STAGING test realtor site for Neighborhood staging (v690): detector v7, ZIP-centroid fallback, and upgrade-request retire.

Public name: **DN Staging Test**. Public email: **wdmtaj@gmail.com**. GitHub repo name stays `bills-fp-realty-co`.

Identity decision note: [docs/site-identity.md](docs/site-identity.md).

## Public URL

- Site: https://dn-stagingtest.netlify.app
- Neighborhood embed: https://dn-stagingtest.netlify.app/neighborhoods

## Snippets (staging only)

Every `sdk.js` and `inline.js` host is `staging.dreamneighborhood.com`. Do not use `app.dreamneighborhood.com` or `www.dreamneighborhoodschools.com`.

| Embed | Snippet |
| --- | --- |
| Popup Neighborhood Explorer | `https://staging.dreamneighborhood.com/explorer/sdk.js` |
| Embedded Neighborhood Explorer | `https://staging.dreamneighborhood.com/explorer/inline.js` (`#dn-explorer`; full variant uses `data-variant="full"`) |
| Popup School Explorer | Same staging SDK (`https://staging.dreamneighborhood.com/explorer/sdk.js`) |
| Embedded School Explorer | Same staging inline (`https://staging.dreamneighborhood.com/explorer/inline.js`) (`#dream-schools-explorer`) |

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
