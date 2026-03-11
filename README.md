# Casa Peptides — Product Catalog

A polished, single-page application for browsing the Casa Peptides product catalog. Built as a zero-dependency, single-file SPA with vanilla HTML, CSS, and JavaScript.

**[View Live Site →](https://casapeptides-catalog.vercel.app)**

## Features

- **127 products across 22 categories** — complete catalog with detailed product information, pricing, and descriptions
- **Hash-based SPA routing** — seamless multi-page navigation (`#/catalog`, `#/category/{name}`, `#/product/{cat}`, `#/compare`) with full browser back/forward support
- **Product detail pages** — individual pages with bottle imagery, pricing breakdowns, size variant selectors, overview/details tabs, and related products
- **Product comparison** — select up to 4 products via checkboxes, compare side-by-side with a "Highlight Differences" toggle to spot variations at a glance
- **Search & filtering** — real-time search across names, catalog numbers, descriptions, and categories; price range filters; multiple sort options (name, price, catalog number)
- **Category tabs** — horizontal scrolling pill-style tab bar for quick filtering by category
- **Card & table views** — toggle between a visual card grid and a compact table layout
- **Light & dark themes** — warm cream/tan light theme and a dark theme, switchable via a toggle in the header
- **Fully responsive** — adapts from 4-column desktop grids down to single-column mobile layouts with a stacked product hero and full-width compare bar

## Tech Stack

- **HTML / CSS / JavaScript** — everything lives in a single file (`Peptide_Catalog.html`) with no build step, no frameworks, and no external dependencies
- **CSS Custom Properties** — full design token system for theming (colors, radii, shadows)
- **Google Fonts** — Red Hat Display and Inter for typography
- **Vercel** — deployed with a simple rewrite rule (`vercel.json`) pointing `/` to `Peptide_Catalog.html`

## Project Structure

```
casa-peptides-catalog/
├── Images/
│   └── Casa-logos/
│       ├── casa 1.png                           # Header logo
│       ├── casa 5.png                           # Footer logo
│       └── bottle_blank_design_transparent.png  # Product detail vial image
├── Peptide_Catalog.html   # The entire application (HTML + CSS + JS)
├── vercel.json            # Vercel rewrite configuration
├── CATALOG_PLAN.md        # Unified redesign & upgrade plan
├── REDESIGN_PLAN.md       # Visual redesign specification
├── UPGRADE_PLAN.md        # Feature upgrade specification
└── .gitignore
```

## Routes

| Route | View | Description |
|---|---|---|
| `#/` or `#/catalog` | Catalog | Main listing with category tabs, search, filters, and product grid |
| `#/category/{name}` | Category | Dedicated category page with scoped filters and products |
| `#/product/{cat}` | Product | Individual product detail page with image, tabs, and variants |
| `#/compare` | Compare | Side-by-side comparison table for 2–4 selected products |

## Running Locally

No build tools or dependencies are required. Simply open the HTML file in a browser:

```bash
# Clone the repository
git clone https://github.com/TomsTools11/casa-peptides-catalog.git
cd casa-peptides-catalog

# Open in your default browser
open Peptide_Catalog.html
```

Or serve it with any static file server for a more production-like experience:

```bash
npx serve .
```

## Deployment

The site is deployed on Vercel and auto-deploys on every push to `main`. The `vercel.json` file contains a single rewrite rule that routes `/` to `/Peptide_Catalog.html`. No build command is needed — Vercel serves the files directly from the repository root.

## License

All rights reserved. This catalog and its contents are proprietary to Casa Peptides.
