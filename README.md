# Faver Fine Art website

This repository publishes the GitHub Pages website for Deirdre Faver's artwork.

Live site: https://buy.faverfineart.com/

## Current structure

- `index.html` contains the live one-page site, including layout, styles, scripts, and embedded painting images.
- `CNAME` points GitHub Pages to `buy.faverfineart.com`.
- `paintings.json` stores artwork and contact data in a cleaner editable format, but the current `index.html` still has the live painting cards hardcoded.

## How to maintain the site today

For small copy, price, contact, or sold-status changes, update the matching text in `index.html` and keep `paintings.json` in sync if the same details appear there.

For new paintings, add the artwork details to `paintings.json`, then add the matching card and image content in `index.html`.

## Recommended next cleanup

The easiest long-term maintenance path is to move painting images into separate image files and have `index.html` render the artwork list from `paintings.json`. That would make future updates much smaller, easier to review, and less error-prone.
