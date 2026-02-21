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


## Model assumptions

The model includes hardcoded diminishing-return constraints:
- CAC worsens with budget scale
- Customer adds saturate toward a monthly cap
- Incremental customer quality declines with scale:
  - ACV decays
  - churn increases
