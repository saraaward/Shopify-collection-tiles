# Shopify Collection Tiles

A configurable Shopify section that turns merchandising destinations into image-led collection tiles.

**Ecommerce creative technology · Merchandising · Reusable web component**<br>
**Status:** public source sample; full host-theme rendering and accessibility review remain outstanding.

[Liquid source](sections/collection-tiles.liquid) · [Sara Ward](https://saraward.ai)

## The Problem

Give an editor a reusable way to feature several collections without editing HTML for each campaign. Show five columns on desktop, then focus the mobile layout on the first three collections.

## What I Built

A section with editable images, labels, links, and block ordering. Editors manage the content through Shopify's theme editor while Liquid and CSS handle the layout.

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

## Workflow

Merchandising priorities and imagery → editor configures tile blocks → Liquid renders the content → CSS adapts the layout → editor reviews the theme preview → publish through the normal theme workflow.

## My Role

Translated a desktop/mobile merchandising layout into a reusable Shopify section with configurable content and ordering.

## Technology

**Shopify Liquid · HTML · CSS Grid · responsive CSS · JSON section schema**

## AI vs Deterministic Logic

The component uses conventional template and layout code. No model or AI service is invoked. The editor supplies the merchandising choices, images, copy, and destinations.

## Setup

1. Add [collection-tiles.liquid](sections/collection-tiles.liquid) to a theme's `sections/` directory.
2. In a compatible section-enabled template, add **Collection tiles (5/3)**.
3. Add tile blocks, choose images, set labels and links, and order the featured collections.
4. Review desktop and mobile layouts in a theme preview before publishing.

The section inherits `--black` and `--font-heading-family` from the host theme. Its CSS selectors are global, so check for naming conflicts during integration.

## QA & Human Oversight

The embedded schema was parsed successfully as JSON on September 15, 2026. The section source was not changed by this documentation update. This does not establish complete theme compatibility or accessibility.

Before using it in a theme, review:

- Desktop and mobile behavior on both sides of the 800px breakpoint.
- First-three mobile ordering, extra desktop rows, and empty or missing images.
- Long labels, cover crops, label contrast, and correct destinations.
- Keyboard access and visible focus for each full-tile link.
- Multiple section instances and interaction with the host theme's styles.

These are integration checks to perform, not claimed completed tests.

## Outcome

The source implements a reusable merchandising section with content controls in the theme editor. No conversion, revenue, or production-deployment outcome is claimed.

## What I Learned

Responsive behavior is also a merchandising decision: hiding tiles on mobile changes which destinations receive attention. The editor's ordering and image composition need to account for that behavior.

## Scope

This repository contains the component source and integration documentation. A full theme and store content are not included.
