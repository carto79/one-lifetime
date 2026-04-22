# One Lifetime · 130 countries, decade by decade

An interactive essay tracing the 130 countries that gained independence between 1926 and 2011 — the lifetime of my grandmother, Faustina Warren Thomas, born in Trinidad in February 1926.

**Live:** _update after deployment_

## Stack

- Single-file static HTML (no build step)
- [D3.js](https://d3js.org/) v7 and [TopoJSON](https://github.com/topojson/topojson) v3 for the interactive world map
- World atlas from [world-atlas@2](https://www.npmjs.com/package/world-atlas) via jsDelivr
- YouTube embed facade (click-to-load) for the 100th birthday video

## Deployment (GitHub Pages)

1. **Settings → Pages** → Source: `Deploy from a branch` → Branch: `main` / `(root)` → Save
2. Wait ~1 minute. Your site is live at `https://<username>.github.io/<repo>/`
3. (Optional) Custom domain: add a `CNAME` file containing just your domain (e.g. `essays.taittfin.com`), then add a DNS CNAME record pointing that subdomain at `<username>.github.io`

## Before going live — update URL references

The JSON-LD, Open Graph, canonical link, and `sitemap.xml` currently reference `https://jtaittw.substack.com/p/one-lifetime` as placeholders. Update these to the final hosted URL once you've chosen where this lives.

In `index.html`, find and replace:
- `https://jtaittw.substack.com/p/one-lifetime` → your canonical essay URL
- `https://jtaittw.substack.com/og/one-lifetime.jpg` → your uploaded 1200×630 share image URL

In `sitemap.xml`, update the `<loc>` to match.

In `robots.txt`, update the `Sitemap:` line to match.

Leave `https://jtaittw.substack.com` (without a path) pointing at Substack — that's correctly identifying your publication hub.

## Post-publish SEO checks

1. [Google Rich Results Test](https://search.google.com/test/rich-results) — paste your URL. Should show "Article" eligibility with zero errors.
2. [Google Search Console](https://search.google.com/search-console) → URL Inspection → Request indexing (forces a crawl in minutes rather than days)
3. Upload a real 1200×630 share image to the `/og/` path before announcing anywhere social

## Credit

Built with Claude Design. Map data: world-atlas. Birthday video: [Jason Taitt on YouTube](https://youtu.be/p1_o9LC24gE).

© 2026 Jason Taitt · JTaitt Writes
