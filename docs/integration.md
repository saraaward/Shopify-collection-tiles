# Integration guide

[Back to project](../README.md) · [Liquid source](../sections/collection-tiles.liquid)

## Setup and theme dependencies

1. Add `collection-tiles.liquid` to a theme's `sections/` directory.
2. In a compatible section-enabled template, add **Collection tiles (5/3)**.
3. Add tile blocks, choose images, set labels and links, and order the featured collections.
4. Review desktop and mobile layouts in a theme preview before publishing.

The section inherits `--black` and `--font-heading-family` from the host theme. Its CSS selectors are global, so check for naming conflicts during integration.

## Behavior

- Desktop uses five columns with a 12px gap; more than five blocks creates additional rows.
- Viewports of 800px or less show three columns and hide blocks after the third.
- Each tile has a 4:5 portrait image area and a full-tile link with an accessible name.
- Images, link labels, destinations, and block ordering are editable in the theme editor.
- The section allows up to 12 blocks and defaults destinations to the store's collection listing.
- Hover treatment applies on devices that support hover.

## Validation status

The embedded schema was parsed successfully as JSON on September 15, 2026. That check establishes schema syntax; full host-theme rendering and accessibility review remain outstanding. The source was not changed during this documentation cleanup.

Before using the section, review:

- Desktop and mobile behavior on both sides of the 800px breakpoint.
- First-three mobile ordering, extra desktop rows, and empty or missing images.
- Long labels, cover crops, label contrast, and correct destinations.
- Keyboard access and visible focus for each full-tile link.
- Multiple section instances and interaction with the host theme's styles.

These are integration checks to perform. No conversion, revenue, or production-deployment result has been measured in this public sample.

## Scope

The repository contains the component source and integration documentation. A complete theme and store content are not included.
