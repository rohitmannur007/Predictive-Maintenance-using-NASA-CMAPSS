# 🛠️ Predictive Maintenance using NASA CMAPSS Dataset

This project focuses on predicting the **Remaining Useful Life (RUL)** of aircraft engines using machine learning. The dataset comes from NASA’s **C-MAPSS** engine degradation simulations. We trained a Random Forest model to estimate how many cycles an engine can operate before failure.

---

## 📁 Dataset

- **Source**: NASA CMAPSS FD001 dataset
- **Type**: Multivariate time series
- **Size**: 100+ engine units, each with 20+ sensors
- **Goal**: Predict Remaining Useful Life (RUL)

---

## 💡 Objective

To build a supervised machine learning model that can:
- Predict the RUL of aircraft engines
- Learn from time-series sensor data
- Help in **predictive maintenance** and reduce unplanned downtime

---

## 🔧 Tech Stack

- **Python**
- **Pandas, NumPy**
- **Scikit-learn**
- **Matplotlib, Seaborn**

---

## 🧪 ML Workflow

1. **Data Preprocessing**
   - Load FD001 dataset
   - Drop irrelevant sensors
   - Normalize sensor values
   - Compute RUL from max cycle

2. **Modeling**
   - Split into train/test
   - Trained **Random Forest Regressor**
   - Evaluated using **RMSE**

3. **Results**
   - **RMSE Achieved**: ~14.3 (lower = better)
   - Accurate trend prediction of engine life

4. **Visualization**
   - Scatter plot of actual vs predicted RUL
   - Time series plots of selected sensors

---

## 📊 Example Output

![RUL Prediction Plot](plots/rul_plot.png)

_(Optional: Add your own graph image here)_

---

## 🧠 Learnings

- Handling time-series sensor data for ML
- Calculating target variable (RUL) for regression
- Feature engineering & normalization
- Importance of model evaluation metrics (RMSE)

---

## 📦 Files in Repo

| File | Description |
|------|-------------|
| `predictive_maintenance.ipynb` | Main notebook with code |
| `README.md` | Project summary |
| `requirements.txt` | Python dependencies |
| `plots/` | Visualizations (optional) |

---

## 🚀 Future Improvements

- Add LSTM/GRU model for deep learning
- Deploy model with Streamlit for interactive predictions
- Train on full CMAPSS (FD002–FD004)

---

## 🤝 Let's Connect

Made with 💙 by **Rohit Mannur**  
👉 [LinkedIn](https://www.linkedin.com) (https://www.linkedin.com/in/rohit-mannur-851a82288/)  
👉 [Email](rohitmannur@gmail.com)

---
