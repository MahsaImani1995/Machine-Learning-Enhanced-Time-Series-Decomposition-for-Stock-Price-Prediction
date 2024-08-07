# Stock Price Prediction Using Machine Learning and Time Series Analysis

This repository contains a comprehensive approach to forecasting stock prices using various machine learning models and time series analysis techniques. The analysis is performed on the stock data of سپیدار from 1399-01-01 to 1402-01-01.

## Table of Contents

- [Introduction](#introduction)
- [Data Collection and Preprocessing](#data-collection-and-preprocessing)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Time Series Decomposition](#time-series-decomposition)
- [Forecasting Models](#forecasting-models)
  - [Simple Moving Average (SMA)](#simple-moving-average-sma)
  - [Random Forest Regression](#random-forest-regression)
  - [LSTM for Residuals](#lstm-for-residuals)
- [Combined Forecast](#combined-forecast)
- [Results and Evaluation](#results-and-evaluation)

## Introduction

Forecasting stock prices is a challenging task due to the inherent noise and volatility in the financial markets. This project aims to leverage different machine learning and statistical methods to predict stock prices and analyze their performance.

## Data Collection and Preprocessing

The historical stock price data is retrieved using the `finpy_tse` library. The data is then preprocessed by:

- Dropping unnecessary columns
- Converting the date column to datetime format
- Setting the date column as the index

The adjusted low prices are plotted to visualize the stock price trend over time.

## Exploratory Data Analysis

An Augmented Dickey-Fuller (ADF) test is performed to check the stationarity of the stock price data. The results include the ADF statistic, p-value, number of lags used, and critical values.

## Time Series Decomposition

The time series data is decomposed into three components:

- **Trend**: Long-term movement in the data
- **Seasonal**: Repeating short-term cycle
- **Residual**: Random variation in the data

Each component is plotted to visualize the different patterns in the stock price data.

## Forecasting Models

### Simple Moving Average (SMA)

The trend component is forecasted using a Simple Moving Average (SMA) model. The window size for the SMA is adjustable. Error metrics such as Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and Mean Absolute Percentage Error (MAPE) are calculated to evaluate the performance.

### Random Forest Regression

The seasonal component is forecasted using a Random Forest Regressor. Features are created using lagged values of the seasonal component. The data is split into training and testing sets, and the model is trained and evaluated. Error metrics are calculated for the forecast.

### LSTM for Residuals

The residual component is forecasted using a Long Short-Term Memory (LSTM) neural network. The data is normalized and split into training and testing sets. The LSTM model is trained and predictions are made. Error metrics are calculated for the forecast.

## Combined Forecast

The final forecast is obtained by combining the predictions from the SMA, Random Forest, and LSTM models. The combined forecast is compared with the actual stock prices for the test set, and error metrics are calculated to evaluate the performance.

## Results and Evaluation

The performance of each model and the combined forecast is evaluated using the following metrics:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Percentage Error (MAPE)

These metrics provide insight into the accuracy of the predictions and the effectiveness of each model. The results are visualized by plotting the actual stock prices and the forecasts.

## Conclusion

This project demonstrates the use of various machine learning and time series analysis techniques to forecast stock prices. The combination of multiple models helps in capturing different patterns in the data, leading to more accurate predictions.

## Dependencies

- Python 3.x
- numpy
- pandas
- finpy_tse
- mplfinance
- scipy
- matplotlib
- statsmodels
- scikit-learn
- keras

## How to Run

1. Clone the repository.
2. Install the required dependencies.
3. Run the script to perform the analysis and generate forecasts.

## Acknowledgements

This project uses the `finpy_tse` library for data retrieval and various machine learning and statistical libraries for analysis and forecasting.

---


