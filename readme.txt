# 🚀 NASA Predictive Maintenance – Predict Machine Failure Like a Rocket Scientist! 🛠️🔬

> ✨ Real sensor data from **NASA turbofan engines** meets cutting-edge ML — predicting failures **before they happen**.

![Python](https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python) 
![XGBoost](https://img.shields.io/badge/XGBoost-Regressor-orange?style=for-the-badge&logo=xgboost)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Predictive%20Maintenance-green?style=for-the-badge&logo=scikit-learn)
![Status](https://img.shields.io/badge/Status-COMPLETE-success?style=for-the-badge)

---

## 🧠 What’s This Project About?

**Mission:** Predict how many engine cycles are left before a failure using real-world jet engine sensor data.

This project helps engineers and businesses **schedule maintenance smartly**, reduce costs, and prevent unexpected breakdowns — just like NASA does!

📈 Problem Type: **Regression (Remaining Useful Life - RUL)**  
📡 Dataset: NASA’s **CMAPSS** engine degradation dataset  
💥 Real Impact: Predicting when machines fail → saving time, money, and lives

---

## 🧰 Tools & Technologies Used

| Category              | Tools / Libraries                        |
|-----------------------|------------------------------------------|
| Programming           | Python (3.10)                            |
| Data Handling         | Pandas, NumPy                            |
| Machine Learning      | Scikit-learn, **XGBoost**                |
| Visualization         | Matplotlib, Seaborn                      |
| Notebook Environment  | Jupyter / Google Colab                   |
| Data Source           | [NASA CMAPSS Dataset](https://www.nasa.gov/content/prognostics-center-of-excellence-data-set-repository) |

---

## 🔍 Dataset Overview

- **Source:** NASA Prognostics Center of Excellence  
- **Use Case:** Turbofan engine sensor analysis  
- **Rows:** Each row = one engine reading at one time step  
- **Important Features:**  
  - `ID` – Engine number  
  - `Cycle` – Time steps  
  - `Sensor 1–21` – Vibration, pressure, temperature, etc.  
  - `Settings` – Operating conditions  
  - `Target` – RUL (manually created)

---

## 🧪 ML Pipeline Breakdown

### 1️⃣ Import Libraries
```python
import pandas as pd
import numpy as np
from xgboost import XGBRegressor
from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_squared_error, r2_score
