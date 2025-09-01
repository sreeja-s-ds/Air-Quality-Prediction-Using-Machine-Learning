# 🌍 Air Pollution Forecasting using Time Series (Prophet)

## 📌 Project Overview
This project focuses on analyzing and forecasting **air pollution levels** across Indian cities.  
The goal is to build a **time-series forecasting model** to predict **Air Quality Index (AQI)** using Facebook’s **Prophet** library.

Key steps include:

- Data Understanding & Cleaning
- Preprocessing (handling missing values, datetime conversion)
- Feature Engineering (pollutant levels, scaling)
- Time-series Forecasting with Prophet
- Model Evaluation (MAE, RMSE, R²)
- Visualization of predictions

## 📂 Dataset
- **Source:** Provided dataset (`air_pollution_data.csv`)
- **Features:**
  - `city`: City name
  - `date`: Recorded date
  - `aqi`: Air Quality Index
  - `co`, `no`, `no2`, `o3`, `so2`, `pm2_5`, `pm10`, `nh3`: Pollutant levels
  - `Datetime`: Processed datetime column (`YYYY-MM-DD HH:MM:SS`)

## ⚙️ Data Preprocessing
- Replaced invalid/missing values with **NaN**
- Filled missing values with **column mean**
- Converted `date` into a **Datetime** column
- Retained pollutant features for modeling
- Scaled features using **StandardScaler**

## 🏗️ Feature Engineering
- Selected important columns:
  - `aqi`, `co`, `no`, `no2`, `o3`, `so2`, `pm2_5`, `pm10`, `nh3`
- Scaled pollutant features for consistency
- Kept `city` and `Datetime` for grouping and visualization

## 🤖 Model Development
- Used **Prophet** for time-series forecasting
- Renamed columns:
  - `Datetime` → `ds`
  - `aqi` → `y`
- Trained Prophet model on historical AQI values
- Forecasted future AQI trends
