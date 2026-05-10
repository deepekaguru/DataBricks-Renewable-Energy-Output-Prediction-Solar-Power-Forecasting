# ⚡ Renewable Energy Output Prediction: Solar Power Forecasting

<img width="919" height="388" alt="image" src="https://github.com/user-attachments/assets/49ca1309-0b66-4911-b749-25c71af7a0f2" />

A production-grade machine learning pipeline built on **Databricks** to predict hourly solar power output based on real weather conditions and temporal patterns. Achieves **99.29% prediction accuracy (R² = 0.9929)**.

---

## 🎯 Project Overview

**Problem:** Grid operators struggle to balance renewable energy supply because solar power output is unpredictable. Accurate forecasting enables better dispatch, reduces curtailment losses, and increases renewable penetration.

**Solution:** End-to-end ML pipeline that:
- Fetches real historical weather data (Open-Meteo API, free)
- Engineers 20+ features including temporal, meteorological, and lagged patterns
- Trains 4 competing models (Linear Regression, Ridge, Random Forest, XGBoost)
- Deploys XGBoost for production with 99.3% accuracy

**Impact:**
- ✅ Enables predictable renewable energy supply for grid balancing
- ✅ Reduces curtailment losses through accurate forecasting
- ✅ Supports decarbonization by improving renewable energy reliability

---

## 📊 Key Results

| Metric | Value |
|--------|-------|
| **Dataset Size** | 168 hours (7 days) of real weather + synthetic solar |
| **Location** | Dallas, Texas (32.78°N, -96.80°W) |
| **Time Period** | June 1-8, 2023 |
| **Best Model** | XGBoost |
| **R² Score** | **0.9929** (99.29% variance explained) |
| **RMSE** | 0.4001 kW |
| **MAE** | 0.2098 kW |

### Model Comparison

```
Linear Regression  →  R² = 0.9908  |  RMSE = 0.4531  |  MAE = 0.3339
Ridge Regression   →  R² = 0.9885  |  RMSE = 0.5083  |  MAE = 0.3831
Random Forest      →  R² = 0.9921  |  RMSE = 0.4208  |  MAE = 0.2345
XGBoost (WINNER)   →  R² = 0.9929  |  RMSE = 0.4001  |  MAE = 0.2098 
```

---

## 🛠️ Technical Stack

**Data & Processing:**
- **Apache Spark** — Distributed data processing at scale
- **Databricks** — Unified ML platform for end-to-end workflows
- **Python** — pandas, numpy, scikit-learn, XGBoost

**Data Sources:**
- **Real Weather Data:** Open-Meteo API (free, no authentication)
  - Temperature, humidity, wind speed, cloud cover
  - Historical hourly data for Dallas, TX
  - 192 hours fetched via API

**ML & Evaluation:**
- scikit-learn (Linear Regression, Ridge, Random Forest)
- XGBoost (gradient boosting regressor)
- sklearn.metrics (RMSE, MAE, R²)

