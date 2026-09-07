# Decision: DN Staging Test identity

William authorized these public values for this STAGING test realtor site. Do not rehash.

## Public name

**DN Staging Test** is the website name a buyer sees (nav, titles, footer, meta, alt text, and docs).

The GitHub repo stays `bills-fp-realty-co`. That repo slug is not the public site name.

This remains a clearly fake / TEST realtor site.

## Public email

**wdmtaj@gmail.com** is the only public contact email.

## Public URL

In-repo links use **https://dn-stagingtest.netlify.app**.

## Snippets

Neighborhood snippets stay on staging:

- `https://staging.dreamneighborhood.com/explorer/sdk.js`
- `https://staging.dreamneighborhood.com/explorer/inline.js` (`#dn-explorer` only)

Embedded School Explorer uses the staging Schools host (Neighborhood `inline.js` does not mount `#dream-schools-explorer`):

- `https://dream-schools-preview-b6b5fcaf4493.herokuapp.com/embed.js`
- mount `#dream-schools-explorer` (minimalist keeps `data-variant="minimalist"`)

Do not add `www.dreamneighborhoodschools.com` or `app.dreamneighborhood.com` unless the staging Schools embed is down.

Featured product surfaces stay popup + embedded School Explorer and Neighborhood Explorer. Nothing else.

`/neighborhoods-narrow` is a 430px-wide column TEST page for staging Neighborhood Explorer chip scroll (sarasotahomes-ish listing column). Same staging `#dn-explorer` + `inline.js` as `/neighborhoods`. Not a production snippet.
