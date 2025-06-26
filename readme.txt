# 🛠️ NASA Predictive Maintenance with Machine Learning

This project uses NASA’s turbofan engine degradation dataset to predict the Remaining Useful Life (RUL) of engines. It applies machine learning (XGBoost) to anticipate engine failure, enabling predictive maintenance and reducing downtime and costs.

---

## 📌 Problem Statement

How many cycles (time units) are left before an engine fails?

Predicting this helps schedule maintenance **before** failure, saving time, money, and improving safety.

---

## 📂 Dataset Overview

- 📁 **Source**: NASA CMAPSS Dataset
- 📊 **Data**: Engine run-to-failure sensor readings
- 🔢 **Features**: 21+ sensors (e.g., temperature, pressure), engine ID, cycles
- 🎯 **Target**: Remaining Useful Life (RUL) = max(cycle per engine) - current cycle

---

## ✅ Project Workflow

### 1. Importing Libraries
Used:
- `pandas`, `numpy` for data handling
- `matplotlib`, `seaborn` for visualization
- `xgboost` for model building

### 2. Load Dataset
Read the CSV file using `pd.read_csv()` and viewed sample records.

### 3. Preprocessing
- Calculated RUL per engine
- Removed unnecessary columns (e.g., unnamed indexes)
- Handled missing values using forward fill (`fillna(method='ffill')`)

### 4. Feature Engineering
- Extracted engine-level patterns
- Normalized continuous features
- Created `RUL` as the prediction target

### 5. Train-Test Split
Split into 75% training and 25% testing using `train_test_split()`.

### 6. Model Training
Trained a **XGBoost Regressor** on the sensor data to predict RUL.

### 7. Evaluation
Used:
- `RMSE` (Root Mean Squared Error)
- `R² Score` for performance

### 8. Visualization
- Plotted predictions vs actual RUL
- Showed feature importance with `xgb.plot_importance()`

---

## 🎯 Key Outcomes

| Metric | Score        |
|--------|--------------|
| RMSE   | ~15 cycles   |
| R²     | ~0.91        |

**Insight**: Model can accurately predict engine failure timeline using only sensor data. Useful for real-world preventive maintenance systems.

---

## 💻 Tools & Technologies Used

- Python (Pandas, NumPy, Matplotlib, Seaborn)
- XGBoost Regressor
- Jupyter Notebook
- NASA CMAPSS Dataset

---

## 📈 Business Value

Predictive Maintenance can:
- 🛫 Prevent sudden breakdowns
- 💰 Save operational & maintenance costs
- 📉 Reduce equipment downtime
- 🧠 Enable data-driven maintenance planning

---

## 🧠 Future Scope

- Build an **LSTM deep learning model**
- Deploy a **real-time dashboard**
- Perform **hyperparameter tuning** for better accuracy

---

## 📎 Links

- 📘 [NASA Dataset Info](https://www.nasa.gov/content/prognostics-center-of-excellence-data-set-repository)
- 📂 GitHub Repo: *Add your repo link here*

---

## 👨‍💻 Author

**Rohit Mannur**  
[LinkedIn](https://linkedin.com/in/rohit-mannur-851a82288) • [GitHub](https://github.com/rohitmannur007) • 📧 rohitmannur@gmail.com

---

> “Stop failures before they stop you.”  
> Predict. Prevent. Perform.
