# One Lifetime · 130 countries, decade by decade

An interactive essay tracing the 130 countries that gained independence between 1926 and 2011 — the lifetime of my grandmother, Faustina Warren Thomas, born in Trinidad in February 1926.

**Live:** _update after deployment_

## Bundle contents

| File | Purpose |
|---|---|
| `index.html` | The essay. Single file, no build step. |
| `one-lifetime-og.jpg` | 1200×630 social share image (Open Graph / Twitter Card / AEO) |
| `grandma-dancing.mp4` | Portrait video, rotation baked in, H.264 + faststart, ~4 MB |
| `grandma-dancing-poster.jpg` | Still poster for the video (shown before user hits play) |
| `robots.txt` | Allows all crawlers, references the sitemap |
| `sitemap.xml` | Sitemap including image and video schema |
| `.nojekyll` | Tells GitHub Pages to serve as-is (skip Jekyll processing) |

## Deployment (GitHub Pages)

1. Drop all files into the root of a new GitHub repo
2. Settings → Pages → Source: `Deploy from a branch` → Branch: `main` / `(root)` → Save
3. Wait ~1 minute. Live at `https://<username>.github.io/<repo>/`
4. (Optional) Custom domain: add a `CNAME` file containing just your domain (e.g. `essays.taittfin.com`), then point a DNS CNAME at `<username>.github.io`

## Before going live — update placeholder URLs

The HTML, sitemap, and robots all reference `https://jtaittw.substack.com` as a placeholder host. Update to your final URL.

**In `index.html`** — find-and-replace these strings with your final URL:

- `https://jtaittw.substack.com/p/one-lifetime` → your canonical essay URL (e.g. `https://essays.taittfin.com/one-lifetime/`)
- `https://jtaittw.substack.com/one-lifetime-og.jpg` → your canonical URL + `/one-lifetime-og.jpg`
- `https://jtaittw.substack.com/grandma-dancing.mp4` → your canonical URL + `/grandma-dancing.mp4`
- `https://jtaittw.substack.com/grandma-dancing-poster.jpg` → your canonical URL + `/grandma-dancing-poster.jpg`

**In `sitemap.xml`** — update the same four URLs.

**In `robots.txt`** — update the `Sitemap:` line to point to your hosted sitemap.

Leave `https://jtaittw.substack.com` (no path) as-is — that correctly identifies your Substack publication hub in the Person/WebSite entities.

## Post-publish checks

1. [Google Rich Results Test](https://search.google.com/test/rich-results) — paste your URL. Should show "Article" eligibility with zero errors, plus detect the VideoObject.
2. [Google Search Console](https://search.google.com/search-console) → add property → URL Inspection → Request indexing.
3. [Meta Sharing Debugger](https://developers.facebook.com/tools/debug/) and [X Card Validator](https://cards-dev.twitter.com/validator) — verify the OG image unfurls correctly on social.
4. [PageSpeed Insights](https://pagespeed.web.dev/) — should score ≥ 95 on both mobile and desktop. The 4 MB video is lazy-loaded via `preload="metadata"`, so it doesn't affect LCP.

## Credit

Interactive map: [D3.js](https://d3js.org/) + [TopoJSON](https://github.com/topojson/topojson) + [world-atlas](https://www.npmjs.com/package/world-atlas).
Dancing footage: LaTasha Brown, Carnival Sunday 2026, Trinidad.
100th birthday video on YouTube: [Jason Taitt](https://youtu.be/p1_o9LC24gE).

© 2026 Jason Taitt · JTaitt Writes
