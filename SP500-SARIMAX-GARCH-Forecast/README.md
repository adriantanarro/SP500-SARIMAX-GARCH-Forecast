# Strategic Forecasting of the S&P 500: A Hybrid SARIMA-GARCH Approach

> **Author:** Adrian Tanarro Musa  
> **Field:** Quantitative Economics & Financial Econometrics  
> **Date:** March 2026  
> **Tech Stack:** Python (`statsmodels`, `arch`, `yfinance`, `fredapi`), Pandas, NumPy, Matplotlib, Seaborn

---

## 1. Executive Summary & Objective

This notebook develops and validates a high-precision forecasting engine for the S&P 500 (SPX). By moving beyond simple trend analysis, this project integrates the structural memory of time-series with the conditional volatility of financial markets.

---

### 2. The Model Architecture: SARIMA(1,0,1) + GARCH(1,1)
The strategy is built on two mathematical pillars:
1. **SARIMA(1,0,1):** Captures the "Autoregressive" memory (up to 1 day) and "Moving Average" shocks, adjusted for seasonality and long-term trends.
2. **GARCH(1,1):** Specifically addresses Volatility Clustering, ensuring that our risk intervals expand during periods of market stress.
3. **Exogenous Regressors ($X$):** The model is "fed" with real-time data from:
    * **DXY (US Dollar Index):** Measuring global liquidity.
    * **VIX (Volatility Index):** Capturing institutional "fear."
    * **10Y Treasury Yields:** Reflecting inflation expectations.

---

### 3. Key Performance Indicators (KPIs)
* **Directional Accuracy (Hit Rate):** ≈ 56.67%
* **MAE Improvement:** +2.19% reduction in error vs. Random Walk ( 46.63 vs 45.62 ).
* **Validation Method:** Unbiased Out-of-Sample Walk-Forward Backtest over a 60-business-day horizon.

---

### 4. Project Structure

```text
├── SP500Forecast_Oficial_ATM.ipynb and .pdf  # Jupyter Notebook with the full proyect
├── requirements.txt                          # Python dependencies
└──  README.md                                # Project documentation



```
