# H&R Block: Leveraged Buyout Analysis

A five-year Excel LBO model evaluating a hypothetical take-private of H&R Block (NYSE: HRB). The analysis connects entry valuation, financing structure, operating forecasts, debt repayment, and sponsor returns.

**Project period:** May–September 2026, with an October 2026 model update.  
**Valuation reference:** October 9, 2026 market data and FY2026 financials.  
**Units:** USD millions, except per-share values and ratios.

## Files and links

- **[Download the Excel model](HRB_LBO_Model_Final.xlsx):** formula-driven workbook with assumptions, sources and uses, operating projections, a debt schedule, and returns.
- **[Read the detailed analysis](https://gist.github.com/prakharss9/60eced64fae448a46358eaf7cfd9e4ec):** project write-up with scenario results and sensitivity tables.

Download the workbook and open it in Microsoft Excel to inspect the formulas. This README assumes the file is uploaded at the repository root under its original filename, `HRB_LBO_Model_Final.xlsx`.

## Investment question

At what acquisition price can a sponsor earn a 20% annual return without relying on excessive leverage or exit-multiple expansion? The 20% hurdle is an analytical assumption, not a financing commitment or a company forecast.

## Key results

| Metric | Base case |
|---|---:|
| Entry EV / EBITDA | 8.0x |
| Entry enterprise value | $8,241 million |
| Implied offer price | $60.81 per share |
| Premium to reference price | 38% |
| Initial debt / EBITDA | 5.0x |
| Debt share of debt-plus-sponsor-equity capitalization | 58.6% |
| Sponsor equity | $3,643 million |
| Exit EV / EBITDA | 8.0x |
| Holding period | 5 years |
| Sponsor IRR | 17.5% |
| Sponsor MOIC | 2.24x |
| Exit debt / EBITDA | 1.9x |

**Conclusion:** pass at an 8.0x entry valuation under the assumed 20% return hurdle. A 7.5x entry with an 8.0x exit produces a base-case IRR of about 21%, but that is a conditional scenario, not an unconditional recommendation to proceed.

The downside case produces a 0.98x MOIC and a negative 0.5% IRR. It highlights the risk of margin compression and a lower exit valuation despite positive interest coverage.

## Model structure

- **Summary:** headline outputs and the investment conclusion.
- **Assumptions:** transaction terms, financing, operating cases, and exit assumptions.
- **LBO Model:** sources and uses, earnings forecast, cash flow, debt repayment, credit metrics, and sponsor returns.
- **Sensitivities:** entry and exit multiple, leverage, IRR, and MOIC analysis.
- **Source Data:** historical financial inputs used in the model.

## Methodology

- **Sources and uses:** sponsor equity is the funding plug after new debt and usable balance-sheet cash; existing debt is refinanced.
- **Debt structure:** a Term Loan B and Senior Notes finance the acquisition. The Term Loan B carries mandatory amortization and a cash sweep; Senior Notes remain outstanding until exit.
- **Cash flow:** EBITDA is reduced by interest, taxes, capital expenditures, and working-capital investment to calculate cash available for debt repayment.
- **Returns:** exit enterprise value less debt plus cash gives equity proceeds. With no interim distributions, MOIC is exit proceeds divided by initial sponsor equity, and IRR is MOIC raised to one-fifth minus one.

## Selected assumptions

| Assumption | Base case |
|---|---:|
| Annual revenue growth | 4.5% |
| EBITDA margin | 26.1% |
| Term Loan B interest rate | 8.0% |
| Senior Notes interest rate | 9.5% |
| Mandatory Term Loan B amortization | 1% of original principal annually |
| Cash sweep | 100% of cash available after mandatory amortization |
| Tax rate | 24% |
| Minimum retained cash | $300 million |
| Transaction fees | 1.5% of entry enterprise value |
| Financing fees | 2.5% of new debt |

These financing terms and forecasts are illustrative assumptions, not lender quotes. The downside case assumes weaker revenue growth, lower margins, and a 6.5x exit multiple.

## How to use

1. Open the workbook in Excel and review the **Assumptions** sheet.
2. Edit blue input cells to test alternative transaction or operating assumptions.
3. Set `Assumptions!B3` to `1` for the base case or `2` for the downside case.
4. Review sponsor returns and credit statistics on **LBO Model**.
5. Check that sources equal uses and that debt and cash balances behave sensibly.

**Sensitivity limitation:** the sensitivity grids are fixed outputs from a Python calculation, not live Excel data tables. They do not refresh when assumptions change.

## Data provenance and limitations

Historical inputs and market values were obtained through Perplexity's finance data tools. The detailed analysis identifies the reference periods, but the repository should not be treated as an audited reproduction of company filings; verify inputs against original filings before professional use.

The model uses beginning-of-year interest balances, simplified working capital, and no interim sponsor distributions. It does not fully capture seasonal liquidity, interest-deductibility restrictions, detailed covenants, or purchase accounting. Positive annual interest coverage alone does not establish financing feasibility.

## Author and disclosure

**Prakhar Singh Sisodia**  
Boston University, Questrom School of Business | Finance & Banking  
[LinkedIn](https://linkedin.com/in/prakharsisodia)
