# 🌬️ AirGuard — Indoor Air Quality Prediction

AirGuard is a machine learning project designed to predict indoor air pollutant concentration (PPM) using environmental and air-quality sensor measurements.

The project follows a complete machine learning workflow, from raw sensor data and exploratory data analysis to model training, evaluation, model saving, and deployment through Streamlit.

---

## 🎯 Problem Statement

Indoor air quality can change due to factors such as humidity, temperature, pressure, and gas-related sensor readings.

AirGuard uses machine learning to estimate **PPM (parts per million)** from multiple environmental and sensor-based features.

The goal is to provide a simple predictive system that can help demonstrate how machine learning can be applied to indoor air-quality monitoring.

---

## 🚀 Project Features

- Data loading and preprocessing
- Missing-value and duplicate checking
- Timestamp-based feature engineering
- Exploratory Data Analysis (EDA)
- PPM distribution analysis
- Correlation analysis
- Multiple machine learning models
- Model performance comparison
- Random Forest feature importance analysis
- Model serialization using Joblib
- Streamlit web application
- Real-time PPM prediction from user inputs

---

## 📊 Dataset

The dataset contains **1,500 observations** and **12 original columns** collected from an IoT-enabled indoor air-quality monitoring system.

### Original Features

| Feature | Description |
|---|---|
| Timestamp | Date and time of measurement |
| Temperature (C) | Temperature in Celsius |
| Humidity (%) | Relative humidity |
| Pressure (hPa) | Atmospheric pressure |
| Gas Resistance (Ohms) | Gas sensor resistance |
| PM2.5 | Fine particulate matter |
| TVOC (ppb) | Total volatile organic compounds |
| eCO2 (ppm) | Equivalent carbon dioxide |
| VOC Index | Volatile organic compound index |
| MQ135 Value | MQ135 gas sensor reading |
| Voltage | Sensor voltage |
| PPM | Target pollutant concentration |

### Dataset Quality

- Total records: **1,500**
- Missing values: **0**
- Duplicate rows: **0**
- Target variable: **PPM**

---

## 🛠️ Data Preparation

The `Timestamp` column was converted into useful time-based features.

Three additional features were extracted:

- Hour
- Minute
- Day

After preprocessing, the dataset contained **13 input features**.

### Final Input Features

```text
Temperature (C)
Humidity (%)
Pressure (hPa)
Gas Resistance (Ohms)
PM2.5
TVOC (ppb)
eCO2 (ppm)
VOC Index
MQ135 Value
Voltage
Hour
Minute
Day
