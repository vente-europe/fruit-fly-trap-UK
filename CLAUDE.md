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

## Key Files
- `index.html` — dashboard (root)
- `Data/x-ray/FF-UK-x-ray.csv` — source data

## Self-Update Rule
Update this file after every bug fix, new tab, or data pattern discovered.
