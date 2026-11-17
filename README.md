# Summit Renovation Group: Kitchen SEO Dashboard

Static dashboard published with GitHub Pages. `index.html` reads `data.json`; nothing else is needed.

## Refreshing

Ask Claude to run the SRG report refresh. It pulls fresh numbers, rewrites `data.json`, commits and pushes, and Pages republishes within a minute or two.

## data.json schema

- `updated`: date of the refresh (YYYY-MM-DD)
- `gsc.start` / `gsc.end`: Search Console window; `start` stays 2025-04-13
- `gsc.clicks`, `gsc.impressions`, `gsc.position`: totals for queries containing "kitchen" over the window
- `gsc.baseline`: the Aug 14, 2026 outlook figures (597 impressions, 38.6 position), kept fixed for comparison
- `gsc.daily`: `[date, impressions]` pairs, zero days omitted
- `gsc.pages`: kitchen-filtered pages, sorted by impressions
- `semrush.history`: monthly snapshots (US database); `semrush.live`: current count

- `ai`: Google generative AI features report (Search Console export, whole site, last 3 months): `daily`, `pages`, `devices`, `us_impressions`. Search Console has no API for this report, so it comes from the manual zip export.

Data sources: Google Search Console (summitrenovationgroup.com) and SEMrush.
