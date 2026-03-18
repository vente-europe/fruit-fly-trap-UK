# Fruit Flies — UK Dashboard

## Purpose
Amazon UK market analysis dashboard for fruit fly traps category.

## Tech Stack
- Single-page HTML dashboard (`index.html`)
- Chart.js 4.4.0 + ChartDataLabels plugin
- Vanilla JS, no build tools

## Data Sources
| Source | Location | Notes |
|--------|----------|-------|
| X-Ray (30d) | `Data/x-ray/FF-UK-x-ray.csv` | 36 ASINs, GBP currency |

## Segments
| Segment | SKUs | Description |
|---------|------|-------------|
| Lure | 10 | Liquid/bait attractant traps (Super Ninja, Zero In) |
| Sticky Trap | 15 | Adhesive paper/card traps (Blooven, aonova, Super Ninja) |
| Electric | 6 | UV/electric zappers (GeckoMan, VEYOFLY, Senelux) |
| Drain | 5 | Drain treatment products (Eco Strong) |

## Data Convention
- **12M estimates** = 30-day X-Ray ASIN Sales/Revenue x 12
- Currency: GBP (£)
- All chart titles include **(12M)**

## Tabs
1. **Main Segments (Total Market)** — segment KPIs, pie charts, summary table
2. **Reviews VOC** — 1,159 reviews across 3 ASINs. Customer Insights (profile, usage, sentiment, motivation, expectations) + Review Browser with filters

## Reviews Tab
- Uses data-driven template pattern from `projects/Dashboards/tab_templates/tabs/reviews-voc.html`
- Only `VOC_DATA` block was customised — rendering engine is standard template code
- Reviews embedded inline (not fetched) for local `file://` compatibility
- Source: `Data/reviews/UK-FF-Reviews.json` (1,159 reviews, 3 ASINs)
- Tagged reviews for browser: `Data/reviews/reviews-browser.json`

## Key Files
- `index.html` — dashboard (root)
- `Data/x-ray/FF-UK-x-ray.csv` — source data
- `Data/reviews/UK-FF-Reviews.json` — raw reviews (JSON, keyed by ASIN)
- `Data/reviews/reviews-browser.json` — tagged reviews for browser

## Self-Update Rule
Update this file after every bug fix, new tab, or data pattern discovered.
