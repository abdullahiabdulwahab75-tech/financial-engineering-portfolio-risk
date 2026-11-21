# Portfolio Risk Measurement and Backtesting Using Python

### An Application of Value at Risk, Expected Shortfall and Monte Carlo Simulation

**Author:** Abdulwahab Abdullahi Adebayo

**Field:** Financial Engineering | Quantitative Finance | Data Analytics

## Project Overview

This project applies Python-based quantitative finance techniques to measure and evaluate the risk and historical performance of a diversified portfolio of five exchange-traded funds (ETFs).

The analysis covers daily market data from January 2020 to December 2025 and demonstrates the practical application of portfolio analytics, statistical risk measurement, Monte Carlo simulation and out-of-sample Value at Risk backtesting.

## Project Objectives

- Examine the volatility and correlation of selected financial assets.
- Construct an equal-weight portfolio.
- Estimate Value at Risk (VaR) using historical and parametric approaches.
- Calculate Expected Shortfall (ES).
- Apply Monte Carlo simulation to estimate multi-day portfolio risk.
- Evaluate portfolio performance using CAGR, volatility, maximum drawdown and Sharpe ratio.
- Conduct out-of-sample VaR backtesting and exact binomial coverage tests.

## Assets Analysed

| Ticker | Asset Exposure |
|---|---|
| SPY | S&P 500 equities |
| QQQ | Nasdaq-100 equities |
| GLD | Gold |
| TLT | Long-term US Treasury bonds |
| EEM | Emerging markets equities |

## Tools and Technologies

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- SciPy
- yfinance

## Methodology

1. Historical adjusted price collection and data quality checks.
2. Daily percentage return calculation.
3. Asset volatility and correlation analysis.
4. Equal-weight portfolio construction with 20% allocation per asset.
5. Historical and parametric VaR estimation.
6. Historical Expected Shortfall calculation.
7. Ten-day Monte Carlo simulation using 20,000 bootstrap paths.
8. Historical ten-day VaR and ES estimation.
9. Portfolio performance and drawdown analysis.
10. Chronological 70/30 training and testing split for VaR backtesting.
11. Exact binomial tests of unconditional coverage.

## Key Findings

### Portfolio Performance

| Metric | Result |
|---|---:|
| Cumulative Return | 93.12% |
| CAGR | 11.63% |
| Annualised Arithmetic Return | 11.98% |
| Annualised Volatility | 13.95% |
| Maximum Drawdown | -26.09% |
| Sharpe Ratio | 0.8590 |

The portfolio achieved positive compounded growth over the observation period, with annualised volatility below that of the most volatile individual asset, QQQ.

### One-Day Risk Estimates

| Confidence | Historical VaR | Historical ES | Parametric VaR |
|---|---:|---:|---:|
| 95% | $134.53 | $202.71 | $139.76 |
| 99% | $215.83 | $341.68 | $199.64 |

Risk estimates are based on a hypothetical $10,000 investment.

### Ten-Day Monte Carlo Results

| Confidence | Monte Carlo VaR | Monte Carlo ES |
|---|---:|---:|
| 95% | $408.96 | $560.24 |
| 99% | $650.74 | $788.00 |

### Out-of-Sample Backtesting

The 70/30 chronological split produced 1,054 training observations and 453 testing observations.

At the 95% confidence level, both VaR models recorded significantly fewer exceptions than expected according to the exact binomial tests. At the 99% level, there was insufficient evidence to reject the expected exception frequency.

## Limitations

- The portfolio uses equal weights rather than an optimised allocation.
- Transaction costs, taxes and management fees are excluded.
- Independent historical resampling in the Monte Carlo simulation does not preserve volatility clustering or temporal dependence.
- Historical ten-day rolling observations overlap.
- The backtesting sample provides limited statistical power at the 99% confidence level.
- The binomial coverage test does not examine exception independence.

## Future Improvements

- Implement portfolio optimisation techniques.
- Introduce GARCH volatility modelling.
- Apply Christoffersen independence and conditional-coverage tests.
- Explore alternative Monte Carlo simulation methods.
- Conduct portfolio stress testing.
- Incorporate transaction costs and rebalancing expenses.

## Repository Contents

`Financial_Engineering_Project_01.ipynb` — Complete Jupyter notebook containing the Python code, analysis, visualisations, results and interpretations.

## Data Source

Historical ETF price data retrieved using the Yahoo Finance Python library (`yfinance`).

## Disclaimer

This project is for educational and portfolio demonstration purposes only. Historical performance and simulated risk estimates do not guarantee future results. This analysis does not constitute investment advice.
