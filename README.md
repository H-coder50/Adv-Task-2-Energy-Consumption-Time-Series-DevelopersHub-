# **⚡Household Energy Consumption Time Series Forecasting**

## 📌 Project Description

This project focuses on **forecasting household energy consumption** using multiple **time series and machine learning models**.
It combines **classical statistical models** and **advanced machine learning approaches** to capture trends, seasonality, and complex patterns in energy usage data.

---

## 🎯 Project Objectives

* Analyze historical energy consumption data
* Perform time-based **feature engineering**
* Visualize trends and seasonality
* Build and compare multiple forecasting models
* Predict future energy consumption accurately

---

## 📊 Dataset Information

* **Dataset:** Household Energy Consumption Dataset
* **Key Features:**

  * Time
  * Global Active Power
  * Global Reactive Power
  * Voltage
  * Global Intensity
  * Sub-metering values

⚠️ The dataset does not contain a full `DateTime` column, so **feature engineering** is applied to make the data suitable for forecasting.

---

## 🛠️ Tools & Libraries

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Statsmodels
* Scikit-learn
* Prophet
* XGBoost

---

## 🔄 Project Workflow

### 1️⃣ Data Preprocessing

* Load dataset
* Handle missing values
* Convert time column into usable format
* Resample data where required

### 2️⃣ Feature Engineering

* Time-based features (hour, lag values, rolling statistics)
* Differencing for stationarity
* Lag and window-based features for ML models

### 3️⃣ Exploratory Data Analysis (EDA)

* Energy usage trends
* Rolling mean and variance
* Seasonal patterns

### 4️⃣ Time Series Decomposition

* Trend
* Seasonality
* Residuals
* Additive vs Multiplicative decomposition

---

## 🤖 Models Used

### 🔹 ARIMA (AutoRegressive Integrated Moving Average)

* Classical statistical time series model
* Captures trend and autocorrelation
* Used after ensuring stationarity

### 🔹 Prophet

* Developed by Facebook
* Handles **seasonality, trends, and missing values** effectively
* Suitable for real-world time series data

### 🔹 XGBoost

* Machine Learning regression model
* Uses lag features and rolling statistics
* Captures **non-linear patterns** in energy consumption

---

## 📈 Forecasting & Evaluation

* Short-term energy consumption forecasting
* Comparison of predictions from:

  * ARIMA
  * Prophet
  * XGBoost
* Evaluation metrics:

  * Mean Absolute Error (MAE)
  * Root Mean Squared Error (RMSE)

---

## 📊 Visualizations Included

* Energy consumption over time
* Rolling statistics plots
* Decomposition plots
* Forecast vs actual comparison plots
* Model comparison plots

(All plots are explained step-by-step in the notebook.)

---

## ✅ Results

* Identified strong **seasonal and trend patterns**
* Prophet handled seasonality effectively
* XGBoost captured complex non-linear relationships
* ARIMA provided a strong statistical baseline
* 
# **Final Conclusion:**

- **XGBoost** performed the best among all models, achieving the lowest MAE (0.446) and lowest RMSE (0.638).
- This indicates that XGBoost predictions are closest to actual energy consumption values with fewer large errors.
- The superior performance of XGBoost is mainly due to:
  - Effective time-based feature engineering (hour, weekday/weekend)
  - Use of lag features, which capture short-term dependencies in energy usage
- For short-term household energy consumption forecasting, XGBoost is the most suitable model, as it provides higher accuracy and better adaptability to complex usage patterns.
---
