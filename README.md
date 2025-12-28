Project Overview

This project focuses on forecasting stock market volatility, a key measure of financial risk, using a hybrid approach that combines statistical time series modeling and deep learning. Instead of predicting stock prices, the project models volatility, which is more stable and meaningful for risk management and decision-making.
The study compares the performance of a traditional GARCH(1,1) model with a Long Short-Term Memory (LSTM) neural network to capture both linear and non-linear temporal patterns in financial time series data.

Dataset

Historical daily stock price data sourced from Yahoo Finance
Adjusted Close prices used to account for corporate actions
Time span: multiple years of daily data
The "yahoo_finance_dataset(2018-2023)" dataset is a financial dataset containing daily stock market data for multiple assets such as equities, ETFs, and indexes. It spans from April 1, 2018 to March 31, 2023, and contains 1257 rows and 7 columns. The data was sourced from Yahoo Finance, and the purpose of the dataset is to provide researchers, analysts, and investors with a comprehensive dataset that they can use to analyze stock market trends, identify patterns, and develop investment strategies.
The dataset can be used for various tasks, including stock price prediction, trend analysis, portfolio optimization, and risk management. The dataset is provided in XLSX format, which makes it easy to import into various data analysis tools, including Python, R, and Excel.

The dataset includes the following columns:

Date: The date on which the stock market data was recorded.
Open: The opening price of the asset on the given date.
High: The highest price of the asset on the given date.
Low: The lowest price of the asset on the given date.
Close: The closing price of the asset on the given date. Note that this price does not take into account any after-hours trading that may have occurred after the market officially closed. Adj Close*: The adjusted closing price of the asset on the given date. This price takes into account any dividends, stock splits, or other corporate actions that may have occurred, which can affect the stock price.
Volume: The total number of shares of the asset that were traded on the given date.

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
