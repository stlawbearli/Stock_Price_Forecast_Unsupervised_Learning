# Stock_Price_Forecast_Unsupervised_Learning
# Stock Price Forecasting — Time Series Analysis ## Overview Time-series forecasting of Apple, Amazon, and DBS stock prices for the next 60 trading days using SARIMA models. Built as part of my Specialist Diploma in Data Science (AI) at Singapore Polytechnic.
---

## Dataset
- Source: CA2-Stock-Price-Data.csv (provided by SP)
- Daily closing prices: October 2018 – September 2023
- 1,257 trading days, no missing values

---

## Approach

### 1. EDA
- Visualised stock price trends over 5 years
- Monthly average resampling to identify seasonal patterns

### 2. Model
- **SARIMA** (statsmodels) fitted independently for each stock
- Seasonal period of 7 (weekly trading cycle)

### 3. Hyperparameter Tuning
- Grid search over seasonal order (P, D, Q, s)
- Best seasonal order for all 3 stocks: (1, 1, 1, 7)

### 4. Results
| Stock | MAE | RMSE | MAPE |
|---|---|---|---|
| Apple | ~13.6 | ~15.7 | 15.6% |
| Amazon | ~15.5 | ~17.3 | 14.4% |
| DBS | ~1.5 | ~1.8 | 1.97% |

---

## Key Findings
- DBS (most stable price range) achieved the best MAPE at ~2%
- Apple and Amazon MAPE (~15%) reflects higher price volatility
- Residuals are approximately normally distributed, indicating good model fit

---

## Files
| File | Description |
|---|---|
| `Stock_Price_Forecasting_THR.ipynb` | Full forecasting notebook |
| `CA2-Stock-Price-Data.csv` | Stock price dataset |

---

## Tools & Libraries
- Python, Pandas, NumPy
- statsmodels (SARIMAX)
- scikit-learn (metrics)
- Matplotlib

---

## Author
**Tan Han Rong**
Specialist Diploma in Data Science (AI), Singapore Polytechnic
