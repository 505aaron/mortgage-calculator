# Mortgage Calculator

Single HTML file mortgage prepayment calculator hosted on GitHub Pages.

## Architecture

- `index.html` — the entire app (HTML + CSS + JS inline)
- Chart.js loaded from CDN
- Query params set personal defaults (balance, payment, extra, 401k, max_extra)
- GitHub Actions workflow deploys to Pages on push to master

## Loan Parameters (hardcoded in index.html)

- Rate, term, 401(k) max, and expected return are constants at the top of the script
- Remaining months calculated via: `n = -ln(1 - balance * r / payment) / ln(1 + r)`

## Key Design Decisions

- Balance and payment are user inputs (not back-calculated) because back-calculation is fragile when extra payments have already been made
- Preset buttons float at bottom of screen so users can toggle scenarios while viewing any chart
- 401(k) and cash projections use the baseline (no-extra-payment) payoff timeline so values are comparable across scenarios
- Wealth comparison chart excludes cash — it's spent on quality of life, not accumulated
- Balance Over Time and Wealth Comparison use log scale for readability
- "Cash Freed Up" shows how much more cash/month vs the current allocation, not a budget remainder
