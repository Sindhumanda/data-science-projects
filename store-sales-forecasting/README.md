#Store Sales Forecasting using AutoARIMA & Prophet

# Problem Statement

Retail businesses require accurate sales forecasts to optimize inventory planning, staffing, and revenue strategy. Poor forecasting can lead to stock shortages, overstocking, and operational inefficiencies.

The objective of this project is to build and compare time-series forecasting models to predict future monthly sales using historical retail data.

# Objectives

- Perform time-series preprocessing and aggregation
- Validate stationarity using Augmented Dickey-Fuller (ADF) test
- Implement automated SARIMA modeling using AutoARIMA
- Implement additive trend-seasonality modeling using Facebook Prophet
- Forecast future sales
- Evaluate model performance using MAE and RMSE
- Compare statistical vs decomposable forecasting approaches

# Dataset

- Source: Kaggle  
- Dataset: `rohitsahoo/sales-forecasting`
- Data aggregated to monthly frequency for improved seasonality modeling.

# Tools & Technologies

- Python
- Pandas & NumPy
- Statsmodels
- pmdarima (AutoARIMA)
- Facebook Prophet
- Scikit-learn
- Matplotlib

# Data Preprocessing
- Converted date column to datetime format
- Aggregated daily sales to monthly totals
- Ensured chronological ordering
- Performed stationarity test (ADF)

# AutoARIMA Model
- Enabled seasonal modeling (`m=12`)
- Automatic selection of optimal `(p,d,q)(P,D,Q)` parameters
- Model selection based on AIC

# Prophet Model
- Reformatted dataset to Prophet schema (`ds`, `y`)
- Modeled trend and seasonality components
- Generated 6-month future forecast

# Model Evaluation
- Evaluated performance using:
  - MAE (Mean Absolute Error)
  - RMSE (Root Mean Squared Error)
- Compared forecast vs actual values visually

# Observations

- Both models successfully captured overall upward sales trend.
- Prophet demonstrated better adaptability to trend shifts.
- AutoARIMA produced smoother, more conservative forecasts.
- Neither model fully captured extreme demand spikes, indicating potential need for external regressors (e.g., promotions, holidays)


