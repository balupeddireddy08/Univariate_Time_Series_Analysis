# Univariate_Time_Series_Analysis with SARIMA Model

## Overview
This Python code demonstrates the process of performing time series analysis using the Seasonal Autoregressive Integrated Moving Average (SARIMA) model. The dataset used in this analysis contains monthly data on the number of airline passengers from 1949 to 1960. The primary objective is to build a SARIMA model to forecast future passenger numbers based on historical data.

## Code Description
### Importing Required Libraries
We begin by importing essential Python libraries such as pandas, numpy, matplotlib, and statsmodels for data manipulation, visualization, and time series analysis.
### Reading the Dataset
We read the airline passenger dataset from a CSV file and inspect the first few rows to understand its structure.
### Exploratory Data Analysis (EDA)
We perform exploratory data analysis to understand the dataset better, including checking data types, data summary statistics, and visualizing the passenger data over time.
### Data Preprocessing
We convert the 'Month' column to a datetime object and set it as the index for time series analysis. Additionally, we specify that the data has a monthly frequency.
### Seasonality Check
We plot the passenger data and mark the December data points with red vertical lines to visualize the seasonality pattern.
### Decomposing the Time Series
We decompose the time series into four components: observed, trend, seasonal, and residual, to gain insights into its various constituents.
### Stationarity Check
We perform a stationarity check using the Augmented Dickey-Fuller (ADF) test. The initial test suggests that the data is non-stationary.
### Automating Stationarity Conversion
We create a function to iteratively difference the data until it becomes stationary based on the ADF test. In this case, differencing the data twice (d=2) makes it stationary.
### Splitting the Data
We split the dataset into a training set (historical data) and a test set (future data to be forecasted).
### Auto ARIMA Model Selection
We use the pmdarima library to automatically select the SARIMA model's parameters that minimize the Akaike Information Criterion (AIC).
### Fitting the SARIMA Model
We fit the SARIMA model to the training data using the chosen parameters.
### Predicting with the SARIMA Model
We use the trained SARIMA model to make predictions on the test dataset.
### Model Evaluation
We evaluate the model's performance using metrics such as mean squared error (MSE), root mean squared error (RMSE), mean absolute error (MAE), and mean absolute percentage error (MAPE).
### Retraining with the Entire Dataset
We retrain the SARIMA model with the entire dataset to prepare for future forecasting.
### Forecasting Future Values
Finally, we use the retrained model to forecast future passenger numbers and visualize the results alongside historical data.
### Output
* The code generates various plots and statistical summaries throughout the process, allowing you to visualize the time series data, seasonality, decomposition, and model performance.
* The SARIMA model is used to forecast future passenger numbers, and the results are plotted alongside the historical data.
### Conclusion
This code demonstrates a comprehensive time series analysis workflow using the SARIMA model for forecasting. It covers data preprocessing, stationarity conversion, model selection, training, evaluation, and forecasting. The SARIMA model is a powerful tool for handling time series data and making accurate predictions.
