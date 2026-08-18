# Detector v7 coverage pages

These extra listing and area pages exist so this STAGING test realtor site can exercise Neighborhood staging (v690) **detector v7** — including ZIP-centroid fallback and upgrade-request retire — against `staging.dreamneighborhood.com`.

They are not inventory. Pages a buyer could mistake for a real offer are labeled **TEST**, **fake brokerage**, and **not a real listing**.

## Why these pages

Detector v7 has to handle more than a clean street slug. The pages below isolate the cases we need on staging:

| Case | Path | Why it is here |
| --- | --- | --- |
| Street in the URL (listing) | `/properties/4401-test-cedar-st-melbourne-fl.html` | Fabricated house. Street is in the slug and the body. |
| No street in the URL (listing) | `/properties/test-listing-8841.html` | Opaque listing ID. Address is only on the page: 2190 Test Palmetto Ave, Fort Pierce, FL 34982. |
| Listing vs area | listings above vs `/neighborhoods/hollywood-hills.html` | Same product popup; listing pages vs neighborhood/area pages. |
| Title-only place name | `/neighborhoods/title-only-place.html` | Place name (`Los Feliz`) is in the document title only, not the heading or body. |
| Hollywood Hills-style area | `/neighborhoods/hollywood-hills.html` | Area name, not a street address. Detector must resolve a neighborhood / area. |
| Doherty-style street-file miss | `/properties/3335-cunningham-rd-le-grand-ca.html` | 3335 Cunningham Rd, Le Grand, CA 95333 is a real MLS house. Our street file is incomplete for Cunningham Rd. Marked as a test listing so it is not treated as inventory. This is the intentional miss path (fallback / retire), not a clean street match. |

Hub: `/neighborhoods/detector-v7.html`.

Existing Florida listings and the 25-page address-embed suite (`/neighborhoods/test-index.html`) stay in place. These pages add the v7-specific gaps, they do not replace that suite.

## What this site does not add

Featured embeds stay exactly these four:

1. Popup School Explorer
2. Embedded School Explorer
3. Popup Neighborhood Explorer
4. Embedded Neighborhood Explorer

No other product surfaces.
