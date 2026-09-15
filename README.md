# Shopify Collection Tiles

A reusable Shopify section for featuring collections with editable images, labels, links, and ordering.

[Liquid source](sections/collection-tiles.liquid) · [Integration guide](docs/integration.md) · [Portfolio](https://saraward.ai)

## What I built

I translated a desktop and mobile merchandising layout into a section editors can manage through Shopify's theme editor.

| Behavior | Implementation |
| --- | --- |
| Desktop | Five columns with a 12px gap |
| Mobile | Three columns at 800px or less; blocks after the third are hidden |
| Images | 4:5 portrait area |
| Content | Editable image, label, destination, and block order |
| Capacity | Up to 12 blocks; more than five creates additional desktop rows |

**Built with:** Shopify Liquid · HTML · CSS Grid · JSON section schema

## Use it

1. Add [collection-tiles.liquid](sections/collection-tiles.liquid) to the theme's `sections/` directory.
2. Add **Collection tiles (5/3)** in a compatible template.
3. Configure the blocks and review the desktop and mobile previews.

The section schema has been parsed as valid JSON. Full host-theme rendering and accessibility review remain outstanding; the [integration guide](docs/integration.md) covers theme dependencies and the checks to complete.

Mobile ordering is a merchandising decision: only the first three destinations remain visible on smaller screens.
