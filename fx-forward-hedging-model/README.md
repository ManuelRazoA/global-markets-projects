# FX Forward Hedging Model

## Objective
Build an Excel-based model to price a theoretical USD/MXN forward and compare hedged versus unhedged FX exposure for a future USD payment.

## Project Overview
This project uses covered interest parity to estimate a theoretical USD/MXN forward rate and evaluates the peso cost of a future dollar payment under two strategies:
- Unhedged exposure
- Hedged exposure using a forward contract

The model shows how a forward contract can lock in the MXN cost of a future USD obligation and reduce foreign exchange uncertainty.

## Files
- `fx_forward_hedging_model.xlsx` — main Excel model
- `fx_forward_summary.pdf` — one-page project summary
- `images/hedged_vs_unhedged_chart.png` — chart used for the repository page

## Key Inputs
- Spot USD/MXN: 17.20
- MXN interest rate: 10.50%
- USD interest rate: 5.25%
- Tenor: 3 months
- Time in years: 0.25
- USD notional: 100,000

## Methodology
1. Start with the current USD/MXN spot rate.
2. Use MXN and USD interest rates together with time to maturity.
3. Estimate the theoretical forward rate through covered interest parity.
4. Compute the MXN cost of hedging the USD notional with the forward.
5. Compare that fixed hedged cost against the unhedged MXN cost under different spot-at-maturity scenarios.
6. Visualize the difference between hedged and unhedged exposure using a scenario chart.

## Main Results
### Forward pricing
- Theoretical forward: 17.422825
- Forward points: 0.222825
- Hedged MXN cost: 1,742,282.54

### Scenario analysis
| Scenario | Spot at Maturity | Unhedged MXN Cost | Hedged MXN Cost | Difference (Hedged - Unhedged) |
|---|---:|---:|---:|---:|
| Scenario 1 | 16.80 | 1,680,000.00 | 1,742,282.54 | 62,282.54 |
| Scenario 2 | 17.20 | 1,720,000.00 | 1,742,282.54 | 22,282.54 |
| Scenario 3 | 17.80 | 1,780,000.00 | 1,742,282.54 | -37,717.46 |
| Scenario 4 | 18.50 | 1,850,000.00 | 1,742,282.54 | -107,717.46 |

## Key Insight
The forward rate is above spot because MXN interest rates are higher than USD interest rates. The hedge removes uncertainty by locking in the peso cost of a future dollar payment. While the hedge may look expensive ex post if spot ends below the forward, it protects against adverse FX moves and stabilizes the expected cash outflow.

## Financial Interpretation
This project highlights that hedging is not about predicting where spot will end, but about reducing risk. Without a hedge, the MXN cost remains exposed to FX fluctuations. With a hedge, the final MXN cost becomes fixed.
