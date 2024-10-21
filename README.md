# Streaming Data Management and Time Series Analysis Project

## Description

- This project aims to analyze streaming data and perform time series analysis to forecast future trends using different statistical and machine learning techniques.
- The dataset, which spans from January 4, 2007, to March 31, 2015, is analyzed using traditional time series models like ARIMA, UCM, and more advanced machine learning methods such as Random Forest, Decision Tree, and Support Vector Regression (SVR).
- The goal is to generate forecasts and compare the performance of various models using metrics like Mean Absolute Error (MAE).

## Pipelines Used :

- Data Collection: The dataset comprises time series data from January 1, 2017, to November 30, 2017, with columns for date and daily consumption values (ave_days).
- Data Preprocessing: This includes handling outliers by replacing extreme values with weekly averages and extracting additional features from the date column such as weekday, day of the month, quarter, and year.
   - Data Standardization: Formatting the time series data consistently.
   - Outlier Handling: Replacing outliers with weekly averages to maintain data integrity.
   - Feature Extraction: Extracting new temporal features from the date column (day of the week, month, year).
- Time Series Models:
   -ARIMA (Auto-Regressive Integrated Moving Average): Initially used for time series forecasting with different parameter configurations.
   - UCM (Unobserved Components Model): Explores trends, seasonality, and residuals.
- Machine Learning Models:
   - Random Forest: Selected for its strong predictive accuracy.
   - Decision Tree: Offers simplicity but with reduced performance.
   - Support Vector Regression (SVR): Tested but less effective.


## Forecasting Pipeline:
- ARIMA: Various configurations were explored, including ARIMA(6,1,5), which yielded the best performance with an AIC of 7322 and an MAE of 1.
- UCM: A random walk with drift was the best-fit level parameter, coupled with 3 sine waves of period 24 and 2 sine waves of period 168 for seasonal components.
- Machine Learning Models: Random Forest outperformed SVR and Decision Tree, achieving an MAE of 11.03.

## Model Evaluation Pipeline:
-Performance Metrics:
   - ARIMA: The best ARIMA model achieved an MAE of 1.
   - UCM: Achieved a MAPE of 11.02% on the test set.
   - Random Forest: Outperformed other machine learning models with an MAE of 11.03.
   - Decision Tree: Performed decently with an MAE of 14.41 but fell short compared to Random Forest.
   - SVR: Underperformed with high error metrics, indicating a poor fit for the dataset.


## Key Findings:
- Trend and Seasonality: ARIMA models captured trends, and UCM identified seasonality patterns in the data.
- Machine Learning Results: Random Forest demonstrated superior accuracy for predictive tasks, while Decision Tree and SVR were less effective.
- Outlier Handling: The method of replacing outliers with weekly averages preserved the integrity of the dataset while minimizing the influence of extreme values.

## Future Work:
- Expanding the dataset to cover more periods could yield more insights.
- Further exploration of machine learning models, such as deep learning architectures (e.g., LSTM, GRU), could improve predictive accuracy.
- Integrating a real-time streaming component for continuous forecasting of time series data.