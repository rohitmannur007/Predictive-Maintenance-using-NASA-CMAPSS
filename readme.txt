# 🚀 NASA Predictive Maintenance – Machine Failure Prediction using ML ⚙️

> Predict equipment failure **before it happens** using real NASA turbofan engine sensor data.  
A Data Science project that blends **engineering intuition with ML power.**

![status](https://img.shields.io/badge/Status-Completed-brightgreen) ![ML](https://img.shields.io/badge/Machine%20Learning-RandomForest-orange) ![Python](https://img.shields.io/badge/Python-3.10-blue)

---

## 📌 Project Overview

Predictive maintenance is critical in industries like aviation, manufacturing, and energy — where failure can cost **millions or even lives**.  
This project uses NASA’s C-MAPSS dataset to predict how many cycles (hours) remain before an engine fails, enabling **preventive action**.

### 🧠 Objective:
> Build a regression model that predicts **Remaining Useful Life (RUL)** of a jet engine based on time-series sensor readings.

---

## 🔧 Tools & Tech Used

- **Language**: Python 3.10+
- **ML Libraries**: Scikit-learn, XGBoost, NumPy, Pandas
- **EDA**: Matplotlib, Seaborn
- **Notebook**: Jupyter
- **Dataset**: NASA C-MAPSS Turbofan Degradation Dataset

---

## 🛠 Dataset Description

- 📂 Source: [NASA Prognostics Center](https://www.nasa.gov/content/prognostics-center-of-excellence-data-set-repository)
- 🧾 Each row = 1 cycle (time step) for 1 engine  
- Features:
  - **ID** – Engine number
  - **Cycle** – Time step
  - **Sensor 1–21** – Vibration, temperature, pressure, etc.
  - **Settings** – Operational conditions
  - **Target (y)** – Remaining Useful Life (manually created)

---

## ⚙️ ML Pipeline Summary

### 1. Import Libraries  
Used Pandas, NumPy, Scikit-learn, Matplotlib, and XGBoost.

### 2. Data Preprocessing
- Combined multiple engine time series
- Engineered `RUL` = max(cycle) - current(cycle)
- Removed non-informative sensors
- Scaled features for better model performance

### 3. EDA + Feature Selection  
- Used `.describe()`, `.corr()`, seaborn heatmaps
- Dropped low-variance or redundant features
- Analyzed sensor degradation patterns

### 4. Model Training
- Used `XGBoostRegressor()` for RUL prediction
- Trained model using 80/20 split
- Evaluated using RMSE, MAE, and R² score

### 5. Feature Importance
- Used XGBoost’s built-in plot to visualize most impactful sensors

---

## 📊 Model Results

| Metric      | Score (example) |
|-------------|-----------------|
| RMSE        | 15.2 cycles     |
| R² Score    | 0.91            |

✅ Model can reliably forecast remaining life across engine types.

---

## 💡 Real-World Impact

- 🔧 Avoid unplanned equipment downtime  
- 📉 Reduce maintenance costs  
- 🛡️ Enhance safety and reliability  
- 🛠 Industrial use cases: aviation, oil & gas, energy, manufacturing

---

## 🌟 What's Next?

- Hyperparameter tuning via GridSearchCV  
- Deep Learning LSTM version (for time series RUL prediction)  
- Deploy as a dashboard with Streamlit or FastAPI

---

## 📁 Project Structure

```bash
NASA-Predictive-Maintenance/
│
├── NASA.ipynb               # Jupyter notebook with full ML pipeline
├── RUL.csv (or your data)   # Preprocessed dataset with sensor data + RUL
├── README.md                # This file
├── requirements.txt         # Dependencies
└── plots/                   # Saved EDA & feature importance visualizations
