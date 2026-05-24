# usd-zar-lstm-forecasting
Multivariate LSTM for USD/ZAR exchange rate forecasting using commodity prices, interest rates, and macro indicators
# USD/ZAR Exchange Rate Forecasting Using Multivariate LSTM

## Overview
This project applies a stacked Long Short-Term Memory (LSTM) neural network
to forecast the USD/ZAR daily exchange rate. The model uses nine input features
across three data categories and is benchmarked against ARIMA and the Random Walk.

## Data Categories
- **Commodity prices:** Gold (GC=F), Platinum (PL=F), Brent Crude (BZ=F)
- **Interest rates:** US Fed Funds Rate, SARB Repo Rate (from FRED)
- **Macroeconomic indicators:** SA CPI, SA REER, US GDP Growth (from FRED)

## Key Results
| Metric | LSTM | ARIMA | Random Walk |
|--------|------|-------|-------------|
| RMSE (log return) | 0.018039 | 0.018111 | 0.018111 |
| MAE (log return) | 0.008135 | 0.008258 | 0.008258 |
| Directional Accuracy | 59.64% | 0.00% | 0.00% |

## Trading Strategy
- Total Return: +1.29% vs Buy-and-Hold +0.75%
- Annualised Sharpe Ratio: 0.5514
- Maximum Drawdown: -0.05%
- Number of Trades: 2

## Feature Importance (Top 3)
1. Gold_Return
2. USDZAR_Return
3. Platinum_Return

## Requirements
```bash
pip install yfinance pandas numpy scikit-learn tensorflow statsmodels
pip install pmdarima matplotlib seaborn pandas-datareader
```

## How to Run
1. Clone the repository
2. Install the requirements above
3. Open `LSTM_Project_v2.ipynb` in Jupyter Notebook
4. Run all cells from top to bottom

## Academic Context
Master of Financial Engineering
Applied Econometrics with Machine Learning
University of Johannesburg — 2025
