# Faver Fine Art website

This repository publishes the GitHub Pages website for Deirdre Faver's artwork.

Live site: https://buy.faverfineart.com/

## Current structure

- `index.html` contains the one-page website layout, style, gallery, About section, and buy buttons.
- `assets/` contains the web-ready artwork photos and artist portrait used by the page.
- `CNAME` points GitHub Pages to `buy.faverfineart.com`.
- `paintings.json` stores artwork and contact data in a clean editable format.
- `paintings.schema.json` documents the expected shape of the artwork catalog.

## How to maintain the site today

For small copy, price, contact, or sold-status changes, update the matching text in `index.html` and keep `paintings.json` in sync if the same details appear there.

For new paintings:

1. Add the web-ready image to the `assets/` folder.
2. Add the artwork details to `paintings.json`, including the image path.
3. Add the matching painting card in `index.html`.

When editing `paintings.json`, keep each painting object in this shape:

```json
{
  "id": 1,
  "title": "Painting title",
  "medium": "Acrylic on canvas",
  "size": "16 × 20 in",
  "price": 199,
  "description": "Short description for the painting.",
  "image": "assets/painting-file-name.jpg",
  "sold": false
}
```

## Recommended next cleanup

The next long-term improvement would be to have `index.html` automatically build the gallery from `paintings.json`. That would make future painting updates even easier because each new painting would only need one image file and one catalog entry.
