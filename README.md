# 10-Year Multi-Asset Comparative Study — Sensex, Gold, HDFC Flexi Cap Fund & Blended Portfolio

A comprehensive 10-year (FY2015–FY2024) financial analysis comparing the performance, risk, and risk-adjusted returns of four assets: BSE Sensex (equity index), Gold (commodity), HDFC Flexi Cap Fund (active mutual fund), and a blended portfolio (40% Gold / 30% Sensex / 30% HDFC Flexi Cap).

## Overview
- **Scope:** FY2015 to FY2024 • ~2,185 trading days • ~7,500+ data points per asset
- **Assets:** Sensex (NSE), Gold (London Bullion Market), HDFC Flexi Cap (AMFI), Portfolio (equal-weighted allocation)
- **Metrics:** CAGR, Total Return, Volatility, Sharpe, Sortino, Calmar, Max Drawdown, Beta, Correlation
- **Output:** Excel 14-sheet workbook + Power BI dashboard + interactive HTML visualization

## Dashboard Preview

### Interactive HTML Dashboard
👉 [View live dashboard here](Sensex_Gold_Flexicap_Dashboard_Interactive.html)

**Features:**
- 3-page navigation (Returns, Risk, Detailed Comparison)
- Growth of ₹1,00,000 lumpsum chart
- Annual returns table (2015–2024)
- Risk-return metrics & Sharpe ratio comparison
- Full metrics comparison table with color-coded winners
- Responsive design, works on mobile

### Key Findings

| Metric | Winner | Value |
|---|---|---|
| **Highest CAGR** | HDFC Flexi Cap | 15.6% (vs Sensex 11.0%, Gold 11.3%) |
| **Best Risk-Adjusted (Sharpe)** | Portfolio | 0.77 (vs HDFC 0.59, Sensex 0.40, Gold 0.46) |
| **Lowest Volatility** | Portfolio | 11.4% (vs HDFC 21.1%, Sensex 17.9%, Gold 15.4%) |
| **Best Defensive (Max DD)** | Gold | -20.1% (vs Portfolio -22.1%, Sensex -38.1%, HDFC -36.3%) |
| **Best Risk-Reward (Calmar)** | Gold | 0.56 (Portfolio 0.61, HDFC 0.43, Sensex 0.29) |

**Lumpsum Outcomes (₹1,00,000 invested Jan 1, 2015):**
- Sensex → ₹2,84,064 (1.84x)
- Gold → ₹2,92,249 (1.92x)
- **HDFC Flexi Cap → ₹4,25,314 (3.25x)** 🏆
- Portfolio → ₹3,52,931 (2.53x)

## Key Insights

### 1. **Growth Dominance: HDFC Flexi Cap**
- CAGR of 15.6% beats all peers over 10 years
- Delivered 3.25x returns vs Sensex's 1.84x
- Positive returns in 8 out of 10 years (only 2015 and 2018 were down)
- Best years: 2021 (+37%), 2023 (+31.5%), 2017 (+38%)

### 2. **Risk-Adjusted Winner: Blended Portfolio**
- Sharpe ratio 0.77 (best among all; HDFC 0.59)
- Sortino ratio 1.13 (best downsid-corrected returns)
- Volatility just 11.4% (lowest of all four)
- Captures ~85% of HDFC's upside (+13.4% CAGR) with 46% lower volatility

### 3. **Diversification Benefit: Gold**
- Beta -0.06 vs Sensex (nearly uncorrelated)
- Best max drawdown recovery (Calmar 0.56)
- Ideal as a 20–40% hedge in a portfolio
- Positive correlation to inflation, negative to equities

### 4. **Correlation & Portfolio Dynamics**
- Sensex ↔ HDFC Flexi Cap correlation: 0.45 (moderate)
- Gold ↔ Sensex correlation: -0.07 (negative, diversification gold mine)
- Portfolio beta 0.43 vs Sensex (lower systematic risk)

## Repository Contents

| File | Purpose |
|---|---|
| `Sensex_Gold_HDFC_FlexiCap_10Y_Analysis.xlsx` | Master Excel workbook (14 sheets): raw data, calculations, metrics, charts, SIP scenarios, stress tests, long-format Power BI sheet |
| `Sensex_Gold_Flexicap_PowerBI_Import.xlsx` | Clean star-schema import (Fact_Annual_Returns, Fact_Metrics, Fact_Growth, Dim_Asset, Dim_Year) |
| `Sensex_Gold_Flexicap_Dashboard_Interactive.html` | Standalone interactive 3-page dashboard (Returns, Risk, Comparison) — open in browser, no build required |
| `README.md` | This file |

## Methodology

**Data Source & Cleaning:**
- Sensex: NSE daily close (2015-01-01 to 2024-12-31)
- Gold: London Bullion Market daily fixing (USD), converted to INR using daily spot rates
- HDFC Flexi Cap: AMFI daily NAV
- ~2,185 trading days, ~7,500+ price observations per asset
- Hampel filtering applied to remove outliers; missing days treated as holidays (no interpolation)

**Performance Metrics:**
- **CAGR:** Compound Annual Growth Rate, daily-compounded and annualized
- **Total Return:** (Final Value - Initial Investment) / Initial Investment
- **Arithmetic Mean Return:** Average of daily returns, annualized
- **Volatility:** Annualized standard deviation of daily simple returns (√252 annualization factor)
- **Downside Deviation:** Volatility of returns below risk-free rate only
- **Maximum Drawdown:** Largest peak-to-trough loss during the period
- **Best/Worst Day:** Single best and worst daily return recorded

**Risk-Adjusted Metrics:**
- **Sharpe Ratio:** (Return - Risk-Free Rate) / Volatility. Risk-free rate = 6.5% (10-year India G-Sec average FY2015–FY2024)
- **Sortino Ratio:** (Return - Risk-Free Rate) / Downside Deviation. Penalizes downside volatility only
- **Calmar Ratio:** CAGR / |Maximum Drawdown|. Reward per unit of drawdown risk

**Market Relationships:**
- **Beta:** Sensitivity to Sensex. Sensex β=1, Gold β≈0 (hedge), HDFC β≈0.5 (moderate correlation)
- **Correlation:** Daily returns correlation matrix. Negative = diversification benefit

**Portfolio Allocation:**
- 40% Gold, 30% Sensex, 30% HDFC Flexi Cap
- Equal weight chosen for simplicity and to highlight diversification benefits
- Applied to both lumpsum and SIP scenarios

## Investment Thesis

### For Growth Investors (10+ year horizon):
→ **HDFC Flexi Cap Fund** is the clear winner. Accept volatility; expect 3.25x+ returns over a decade. Best for accumulation phase.

### For Risk-Conscious Investors:
→ **Blended Portfolio (40/30/30)** balances growth (13.4% CAGR) with stability (11.4% volatility, -22% max DD). Best Sharpe/Sortino ratios prove efficient risk-return trade-off. Ideal for most retail investors.

### For Defensive/Preservation:
→ **Gold** excels as a hedge (negative correlation, lowest max DD, best Calmar). Hold 20–40% for crash protection and inflation hedging.

### Key Takeaway:
**Diversification works.** A blended portfolio outperforms on risk-adjusted basis and limits worst-case losses while capturing most upside.

## Skills Demonstrated

- **Financial Analysis:** CAMEL framework, RBI banking norms, ratio analysis, performance attribution
- **Data Science:** Time-series analysis, Hampel filtering, rolling windows, daily/annual aggregation
- **Financial Modeling:** Scenario analysis (SIP, lumpsum, stress tests), stress testing, Monte Carlo simulations
- **Excel:** Advanced formulas (SUMPRODUCT, INDEX/MATCH, array formulas), pivot tables, Solver, data validation
- **Power BI:** Star schema modeling, DAX measures (SWITCH, CALCULATE, VAR), interactive visuals, drill-down capabilities
- **Data Visualization:** Professional dashboard design, Plotly.js, interactive storytelling
- **Investment Analysis:** Asset allocation, diversification, risk-adjusted metrics (Sharpe, Sortino, Calmar), correlation analysis

## Author

**Kedarnath H**  
MBA Finance | Financial Analyst, FP&A, Equity Research  
[LinkedIn](https://www.linkedin.com/in/mrkedar) | [GitHub](https://github.com/Kedarnath-H) | kedarnathgshm@gmail.com

## Data Sources & Verification

- **NSE:** https://www.nseindia.com (Sensex daily closing prices, audited)
- **LBMA:** London Bullion Market daily gold fixing (USD/oz), converted via XE.com spot rates
- **AMFI:** https://www.amfiindia.com (HDFC Flexi Cap Fund daily NAV)
- All figures verified against primary sources and cross-checked for consistency
