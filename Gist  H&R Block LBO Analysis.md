# H&R Block (HRB): Leveraged Buyout Analysis

**Independent academic project** | Boston University, Questrom | Market data as of Oct 9, 2026 | $ in millions unless noted

> Illustrative exercise, not investment advice. Interest rates, leverage, fees, tax rate and operating cases are my own assumptions, not market quotes.

## Summary
I modeled a hypothetical take-private of H&R Block (NYSE: HRB) with a 5-year hold and an exit at the end of FY2031 (fiscal year ends June 30).

| Metric | Base case |
|---|---|
| Entry EV / FY2026 adj. EBITDA | **8.0x** (EV $8,241) |
| Implied offer price / premium | **$60.81** per share, **38%** premium to $44.05 |
| Leverage | **5.0x** EBITDA (Term Loan B 3.0x, Senior Notes 2.0x) = $5,151 |
| Sponsor equity | $3,643 (41% of capitalization) |
| Exit multiple | 8.0x FY2031 EBITDA |
| **IRR / MOIC** | **17.5% / 2.24x** |
| Downside case IRR / MOIC | -0.5% / 0.98x |

## Recommendation
**Pass at 8.0x; proceed at or below 7.5x EV/EBITDA.**
- At 8.0x (a 38% premium) the base-case IRR of 17.5% is below a typical 20% sponsor hurdle (my assumption), and the downside case returns about 1.0x.
- At 7.5x entry (about a 29% premium) the base-case IRR is about 21% at an 8.0x exit.
- Debt capacity is adequate: EBITDA / cash interest stays above 2.2x even in the downside, and leverage falls from 5.0x to 1.9x by FY2031 in the base case.
- Key risks: seasonal tax-prep revenue, competition from DIY software, and sensitivity to the exit multiple.

## Transaction structure
| Sources | $mm | Uses | $mm |
|---|---|---|---|
| Term Loan B (3.0x) | 3,090 | Purchase of equity | 7,708 |
| Senior Notes (2.0x) | 2,060 | Refinance existing debt | 1,491 |
| Balance sheet cash used | 659 | Transaction fees (1.5% of EV) | 124 |
| Sponsor equity | 3,643 | Financing fees (2.5% of new debt) | 129 |
| **Total** | **9,452** | **Total** | **9,452** |

## Key assumptions
- **Base operating case:** revenue growth of 4.5% a year (HRB's FY2023 to FY2026 revenue CAGR was about 4.3%); EBITDA margin held at the FY2026 level of 26.1%.
- **Downside case:** revenue growth of 0% to 2%, EBITDA margin falls to 23.5% to 24.5%, exit multiple 6.5x.
- **Financing:** Term Loan B at 8.0% (1% mandatory amortization, 100% cash sweep); Senior Notes at 9.5% (bullet). Interest is computed on beginning balances.
- **Other:** tax rate 24%; D&A 3.1% and capex 2.1% of revenue; change in NWC is 5% of the change in revenue; minimum cash $300mm; financing fees amortized over 7 years.

## Base-case projections
| | FY2027E | FY2028E | FY2029E | FY2030E | FY2031E |
|---|---|---|---|---|---|
| Revenue | 4,123 | 4,308 | 4,502 | 4,705 | 4,917 |
| EBITDA | 1,076 | 1,125 | 1,175 | 1,228 | 1,283 |
| Total debt / EBITDA | 4.4x | 3.8x | 3.2x | 2.5x | 1.9x |
| EBITDA / cash interest | 2.4x | 2.7x | 3.2x | 3.8x | 4.6x |

## Sensitivities (base case)
**IRR: entry multiple vs. exit multiple (5.0x leverage)**

| Entry \ Exit | 7.0x | 7.5x | 8.0x | 8.5x | 9.0x |
|---|---|---|---|---|---|
| **7.0x** | 21.5% | 23.7% | 25.8% | 27.7% | 29.5% |
| **7.5x** | 17.1% | 19.3% | 21.2% | 23.1% | 24.8% |
| **8.0x** | 13.6% | 15.6% | 17.5% | 19.3% | 21.0% |
| **8.5x** | 10.6% | 12.6% | 14.4% | 16.2% | 17.8% |
| **9.0x** | 8.0% | 9.9% | 11.7% | 13.4% | 15.1% |

**MOIC: entry multiple vs. exit multiple (5.0x leverage)**

| Entry \ Exit | 7.0x | 7.5x | 8.0x | 8.5x | 9.0x |
|---|---|---|---|---|---|
| **7.0x** | 2.65x | 2.90x | 3.14x | 3.39x | 3.64x |
| **7.5x** | 2.21x | 2.41x | 2.62x | 2.82x | 3.03x |
| **8.0x** | 1.89x | 2.07x | 2.24x | 2.42x | 2.59x |
| **8.5x** | 1.65x | 1.81x | 1.96x | 2.11x | 2.27x |
| **9.0x** | 1.47x | 1.61x | 1.74x | 1.88x | 2.02x |

**IRR: leverage vs. entry multiple (8.0x exit)**

| Leverage \ Entry | 7.0x | 7.5x | 8.0x | 8.5x | 9.0x |
|---|---|---|---|---|---|
| **4.0x** | 21.7% | 18.4% | 15.6% | 13.2% | 11.0% |
| **4.5x** | 23.5% | 19.7% | 16.5% | 13.8% | 11.4% |
| **5.0x** | 25.8% | 21.2% | 17.5% | 14.4% | 11.7% |
| **5.5x** | 28.9% | 23.2% | 18.8% | 15.2% | 12.2% |
| **6.0x** | 33.4% | 26.0% | 20.6% | 16.3% | 12.8% |

## Data sources and limitations
- FY2023 to FY2026 revenue, adjusted EBITDA, debt, cash, share price and market cap from Perplexity finance data (annual financial statements, adjusted metrics, quotes), market data as of Oct 9, 2026.
- No interim dividends, no circular interest calculation, and seasonal working capital is simplified to a flat share of revenue growth.
- The sensitivity tables were computed with a Python replica of the Excel model, which matches the Excel model at base and downside inputs.

## Files
The full Excel model (live formulas, scenario switch, sources & uses, debt schedule) is available on request: prakhars@bu.edu.

*Author: Prakhar Singh Sisodia, Boston University (Questrom), Finance & Banking. [LinkedIn](https://linkedin.com/in/prakharsisodia)*
