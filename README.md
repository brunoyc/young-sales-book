# YOUNG.Sales — The Sales Book

Static, self-contained landing page for the YOUNG Group's internal commercial catalog: 53 entries across 13 parts (Workspaces, Hospitality, Real Estate, Media, Studio, Products, Deals, Loyalty, Expansion, Ecosystem Packages, Sales Directory), plus a Sales Process section explaining how each business vertical sources, qualifies, and closes leads.

Built from `catalog-data.json` and styled to the YOUNG.Sales brand design system (Klein blue, Ink, Steel, Instrument Serif / IBM Plex Mono, no radius or shadow).

## Stack

Everything — CSS, fonts (as base64 `@font-face` data URIs), and the catalog data (as embedded JSON) — lives in one file: `index.html`. No build step, no dependencies, no backend. Search and filtering run client-side in vanilla JS.

## Deploy

This is a zero-config static site. On Vercel: **New Project → Import this repo → Deploy** — no framework preset or build command needed, `index.html` at the root is served as-is.

## Updating the catalog

To update the data, regenerate `index.html` from a fresh `catalog-data.json` (the embedded `<script type="application/json" id="catalog-data">` block) rather than hand-editing — the JSON is a straight copy-paste of the source file.

Internal use only — not for external distribution.
