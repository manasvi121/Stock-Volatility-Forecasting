Project Overview

This project focuses on forecasting stock market volatility, a key measure of financial risk, using a hybrid approach that combines statistical time series modeling and deep learning. Instead of predicting stock prices, the project models volatility, which is more stable and meaningful for risk management and decision-making.

The study compares the performance of a traditional GARCH(1,1) model with a Long Short-Term Memory (LSTM) neural network to capture both linear and non-linear temporal patterns in financial time series data.

Dataset

Historical daily stock price data sourced from Yahoo Finance
Adjusted Close prices used to account for corporate actions
Time span: multiple years of daily data

Methodology

Data Preprocessing
Converted stock prices to log returns to achieve stationarity
Performed time-based train–test split to prevent data leakage
Exploratory Data Analysis
Visualized volatility clustering using rolling standard deviation
Analyzed return distributions and ARCH effects
Statistical Modeling
Implemented GARCH(1,1) to model conditional volatility
Generated volatility forecasts on unseen test data
Deep Learning Modeling
Used GARCH-estimated volatility as input to an LSTM model
Applied sliding window technique and normalization
Trained with Early Stopping to avoid overfitting

Evaluation

Compared GARCH and LSTM models using RMSE and MAE
Visualized predicted vs actual volatility

Key Insights

GARCH effectively captures volatility clustering and persistence
LSTM learns complex, non-linear temporal dependencies
LSTM achieved lower forecasting error, while GARCH provided strong interpretability
Hybrid modeling improves robustness of volatility forecasts

Tools & Technologies

Python, NumPy, Pandas
Statsmodels, ARCH
TensorFlow / Keras
Scikit-learn
Matplotlib
