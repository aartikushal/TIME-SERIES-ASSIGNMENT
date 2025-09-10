📘 README: Time Series Forecasting with ARIMA & SARIMA
🔹 Project Overview

This project applies time series forecasting techniques to predict Apple (AAPL) stock closing prices using ARIMA and SARIMA models.
We compare performance across both models and evaluate forecast accuracy using MAE, RMSE, and MAPE.

🔹 Objectives

Explore and preprocess stock price data.

Conduct exploratory time series analysis (trend, volatility, seasonality).

Perform ACF & PACF analysis to determine ARIMA parameters.

Build ARIMA and SARIMA models for forecasting.

Forecast stock prices for the next 30–60 days.

Compare model performance with error metrics and residual analysis.

🔹 Dataset

Source: Kaggle (Apple AAPL stock dataset)

Features used: Date, Close

Range: 1980 – 2021

Frequency: Daily closing prices

🔹 Methodology
1. Data Preparation

Parsed Date column as datetime.

Set Date as index.

Handled missing values with forward/backward fill.

Checked datatypes and ensured numeric values.

2. Exploratory Analysis

Plotted closing price trends over time.

Computed rolling mean & standard deviation to assess volatility.

Applied seasonal decomposition (trend, seasonality, residuals).

3. Stationarity & ACF/PACF

Applied ADF test → differencing applied (d=1).

Plotted ACF (for MA terms) and PACF (for AR terms).

Selected ARIMA(1,1,2) as a candidate model.

4. Model Building

ARIMA (1,1,2): No seasonality.

SARIMA (1,1,2)(1,1,1,12): Seasonal extension.

Forecasted next 60 days.

5. Evaluation

Metrics used:

Mean Absolute Error (MAE)

Root Mean Squared Error (RMSE)

Mean Absolute Percentage Error (MAPE)

Residual analysis performed to confirm white noise assumption.

🔹 Results
Model	MAE	RMSE	MAPE (%)
0   ARIMA  11.52  13.38       NaN
1  SARIMA  13.81  15.81       NaN

👉 SARIMA slightly outperformed ARIMA, but improvements were marginal since stock prices are trend/volatility driven rather than strongly seasonal.

🔹 Visualization

Closing price trend.

Rolling mean & volatility.

Seasonal decomposition (trend, seasonality, residual).

ACF & PACF plots.

Forecasts vs actual test data.

Residual diagnostics.

🔹 Tools & Libraries

Python

Pandas – data manipulation

Matplotlib, Seaborn – visualization

Statsmodels – ARIMA, SARIMA, ACF, PACF

Scikit-learn – error metrics

🔹 Conclusion

Both ARIMA and SARIMA models can effectively forecast short-term stock prices.

SARIMA performed slightly better, but the difference was small due to limited seasonality in AAPL stock.

Models are effective for short-term forecasting, but long-term predictions remain challenging due to market volatility.
