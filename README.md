# Unit Economics Model

A lightweight, single-file interactive unit economics simulator for B2B SaaS planning.

It models how acquisition spend impacts:
- revenue
- contribution
- total cost
- net cash flow
- cash balance
- NPV and marginal NPV

The app is built as a static HTML page with D3.js and no build step.

## What it includes

- Two-panel chart:
  - top: monthly flow lines (Revenue, Contribution, Total cost, Net cash flow)
  - bottom: cash balance over time
- Fixed right-side legends aligned to each line endpoint
- Sticky chart column with independently scrollable inputs/metrics column
- Input popovers and model formula panel
- Budget optimizer with an NPV objective over slider range

## Model assumptions

The model includes hardcoded diminishing-return constraints:
- CAC worsens with budget scale
- Customer adds saturate toward a monthly cap
- Incremental customer quality declines with scale:
  - ACV decays
  - churn increases

## Run locally

Open `spend.html` directly in your browser:

```bash
open spend.html
```

Or serve the folder with any static server:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Project structure

- `spend.html` - entire app (UI, model, D3 rendering)
- `README.md` - project documentation

## Notes

- This is a planning model, not accounting software.
- Results are sensitive to assumptions and horizon length.
