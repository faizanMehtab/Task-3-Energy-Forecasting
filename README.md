# Time Series Forecasting Project (ARIMA, Prophet, XGBoost)

##  Project Overview

This project focuses on forecasting **hourly household energy consumption** using multiple time series and machine learning models. The objective is to analyze historical power usage patterns and compare different forecasting approaches based on performance metrics.

The project was completed as part of a **Data Science task/internship assignment** and follows proper data preprocessing, modeling, evaluation, and comparison steps.
zip file of complete task is given because of large data set.
---

##  Dataset Description

**Dataset:** Household Power Consumption Dataset

### Columns Used:

* `Date` – Date of measurement
* `Time` – Time of measurement
* `Global_active_power` – Total active power consumed (target variable)
* Other electrical measurements (reactive power, voltage, intensity, sub-metering)

The data was converted into **hourly time series** for analysis.

---
##  Data Preprocessing

* Combined `Date` and `Time` into a single datetime column
* Set datetime as index
* Converted all numeric columns from object to float
* Handled missing values by dropping NaNs
* Resampled data to **hourly mean consumption**

---

##  Feature Engineering

The following features were created:

* Hour of the day
* Day of the week
* Weekend indicator
* Lag features (previous 1, 2, and 3 hours)

These features help capture temporal and sequential patterns in energy usage.

---

##  Models Implemented

### ARIMA (AutoRegressive Integrated Moving Average)

* Classical statistical time series model
* Captures linear trends and temporal dependencies
* Evaluated using MAE and RMSE

### Prophet

* Time series forecasting model developed by Meta (Facebook)
* Automatically handles seasonality and trend changes
* Suitable for business time series data

### XGBoost Regressor

* Machine learning-based approach
* Uses lag features and time-based features
* Captures nonlinear relationships effectively

---

## 📈 Evaluation Metrics

All models were evaluated using:

* **MAE (Mean Absolute Error)**
* **RMSE (Root Mean Squared Error)**

NaN values produced during forecasting were carefully removed before evaluation to ensure accurate metric calculation.

---

##  Model Comparison

| Model   | Strengths                                                   |
| ------- | ----------------------------------------------------------- |
| ARIMA   | Simple, interpretable, good for linear patterns             |
| Prophet | Handles seasonality and trend shifts well                   |
| XGBoost | Best performance due to nonlinear learning and lag features |

**XGBoost achieved the lowest error**, making it the most accurate model for this dataset.

---

##  Key Learnings

* Proper preprocessing is critical for time series modeling
* Classical and ML models require different data preparation
* Lag features are essential for ML-based forecasting
* Handling NaN values is necessary before evaluation

---

##  Libraries Used

* pandas
* numpy
* matplotlib
* scikit-learn
* statsmodels
* prophet
* xgboost

---

##  Conclusion

This project demonstrates a complete time series forecasting pipeline, from raw data preprocessing to advanced model comparison. The results show that machine learning models like XGBoost can outperform traditional statistical models when sufficient features are engineered.

---
