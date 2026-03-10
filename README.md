# Fixed Income Sensitivity Model

## Objective
Build an Excel-based model to price a 5-year coupon bond and evaluate its sensitivity to changes in yields.

## Project Overview
This project prices a plain-vanilla coupon bond using discounted cash flows and then measures interest rate sensitivity through:
- Macaulay Duration
- Modified Duration
- Convexity
- Approximate repricing under yield shocks
- Exact repricing under yield shocks
- Price-yield visualization

## Files
- `fixed_income_sensitivity_model.xlsx` — main Excel model
- `fixed_income_summary.pdf` — one-page project summary
- `images/price_yield_chart.png` — chart image for the repository page

## Key Inputs
- Face value: 1000
- Annual coupon rate: 8.0%
- Maturity: 5 years
- Payments per year: 2
- Yield to maturity: 10.0%

## Methodology
1. Estimate coupon payments and total cash flows by period.
2. Discount all cash flows using the yield per period.
3. Sum present values to obtain the bond price.
4. Compute Macaulay Duration as the weighted average time of discounted cash flows.
5. Convert Macaulay Duration into Modified Duration to approximate percentage price sensitivity.
6. Compute Convexity to improve the approximation for non-linear price-yield effects.
7. Compare approximate repricing against exact repricing for +50 bps, +100 bps, and -50 bps shocks.
8. Plot the price-yield relationship to visualize the inverse and convex relation between price and yield.

## Main Results
### Base valuation
- Bond price: 922.78
- Macaulay Duration: 4.1798
- Modified Duration: 3.9808
- Convexity: 19.5736

### Scenario analysis
| Scenario | New Yield | Approx Price | Exact Price | Approx Error | Duration-Only Price |
|---|---:|---:|---:|---:|---:|
| +50 bps | 10.5% | 904.642 | 904.639 | 0.002 | 904.416 |
| +100 bps | 11.0% | 886.952 | 886.936 | 0.016 | 886.049 |
| -50 bps | 9.5% | 941.375 | 941.377 | -0.002 | 941.150 |

## Key Insight
Bond prices move inversely to yields. Duration provides a first-order approximation of price sensitivity, while convexity improves the estimate because the price-yield relationship is curved rather than linear.
