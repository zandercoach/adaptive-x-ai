# Design — the journal site

The site follows the zander.coach corporate design (`CORPORATE-DESIGN.md` in Christian's workspace; reference implementation: the website theme `zander`). Tokens, fonts and elements are in `assets/site.css`. This file holds only what the site adds to that core.

## Sub-brand — *2026-11-08*

Adaptive × AI is a sub-brand of zander.coach: own name, own mark, the core design throughout.

- **The × is the mark.** In the title in Petrol, as the favicon, and as the bullet of every list — in the place the signet takes on zander.coach. Reason: the site has its own name and carries its own sign; the signet stands for the endorsement, not for the page.
- **The endorsement** stands in the footer: the signet, negative (Paper on Tiefsee), and „A journal by zander.coach". Nowhere else.
- **No navigation header.** Two pages, linked in the text and in the eyebrow.

## Assets

- `assets/fonts/` — Epilogue and Spectral as woff2, copied from the theme, with their OFL licences. Refresh them when the theme's fonts change.
- `assets/highlight.webp` — the highlighter stroke, copied from the theme. It works as a CSS mask and therefore only over HTTP, not from `file://`.
