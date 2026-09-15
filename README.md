# Shopify Collection Tiles

**Ecommerce creative technology · Merchandising · Reusable Liquid section**

A configurable homepage section that turns a set of merchandising destinations into image-led collection tiles.

**My contribution:** translating a desktop/mobile merchandising layout into a Shopify section with editable images, labels, links, and block ordering.

[View the Liquid source](sections/collection-tiles.liquid) · [Sara Ward](https://saraward.ai)

## The merchandising requirement

Give an editor a reusable way to feature several collections without editing HTML for each campaign. Show five columns on desktop, then focus the mobile layout on the first three collections.

## Current behavior

| Setting or behavior | Implementation |
| --- | --- |
| Desktop layout | Five columns with a 12px gap |
| Mobile layout | Three columns at viewport widths of 800px or less; blocks after the third are hidden |
| Tile proportion | 4:5 portrait image area |
| Editable content | Background image, link label, destination URL |
| Ordering | Order of blocks in the theme editor |
| Block capacity | Up to 12; more than five creates additional desktop rows |
| Default destination | The store's collection listing |
| Interaction | Full-tile link with an accessible name; hover treatment on devices that support hover |

## Use in a theme

1. Add [collection-tiles.liquid](sections/collection-tiles.liquid) to a theme's `sections/` directory.
2. In a compatible section-enabled template, add **Collection tiles (5/3)**.
3. Add tile blocks, choose images, set labels and links, and order the featured collections.
4. Review desktop and mobile layouts in a theme preview before publishing.

The section inherits `--black` and `--font-heading-family` from the host theme. Its CSS class selectors are global, so check for naming conflicts when integrating it into another theme.

## Design decisions and limits

- The mobile view prioritizes the first three blocks. Editors should place their most important destinations first.
- Images use a cover crop; source composition needs room for the crop and overlaid label.
- The image area is portrait despite the original working file's name, `first edit to square`.
- This is an existing source sample. The curation renamed the file and added documentation; its Liquid, CSS, and schema behavior are unchanged.

**Validation:** the source was verified byte-for-byte against the existing public file, and the embedded schema was parsed as JSON. A full theme rendering and accessibility review was not performed during this curation.
