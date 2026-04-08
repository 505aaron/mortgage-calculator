# Mortgage Prepayment Calculator

A single-page mortgage prepayment and budget allocation calculator. Compare scenarios for extra mortgage payments, 401(k) contributions, and cash savings — with interactive charts.

## Usage

Open the GitHub Pages URL with query parameters to set your defaults:

```
https://505aaron.github.io/mortgage-calculator/?rate=7.0&bal=300000&pmt=2000&extra=500&fourk=1000&max_extra=2000
```

### Query Parameters

| Param | Description | Default |
|-------|-------------|---------|
| `rate` | Annual interest rate (e.g. 4.875) | **required** |
| `bal` | Current mortgage balance | 300000 |
| `pmt` | Monthly P&I payment | 2000 |
| `extra` | Current extra mortgage payment | 0 |
| `fourk` | Current 401(k) contribution | 1000 |
| `max_extra` | Max extra payment (aggressive slider limit) | 2000 |

Without parameters, the calculator loads with generic defaults.

### Preset Scenarios

Floating buttons at the bottom let you quickly toggle between:

- **Current** — your current allocation
- **Max 401(k)** — max out retirement contributions
- **Aggressive** — maximize extra mortgage payments
- **More Cash** — reduce extra payments, free up cash

### Charts

- **Balance Over Time** (log scale) — baseline vs extra payment payoff curves
- **Monthly Payment Breakdown** — principal / interest / extra stacked bars
- **Wealth Comparison** (log scale) — 401(k) growth vs cumulative interest saved

## Tech

- Single HTML file (`index.html`)
- Chart.js from CDN
- All math runs client-side, no server
- Mobile-first responsive design

## Development

Just edit `index.html` and push. GitHub Pages auto-deploys from `master`.
