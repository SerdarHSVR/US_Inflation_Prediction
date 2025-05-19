# 🧮 U.S. Inflation Prediction Using Macroeconomic Indicators (2000–2023)

### 📊 Final Project – ADS 577 | Applied Data Science  
**Author:** Serdar Hoşver  
**University:** TED University, Applied Data Science  
---

## 📌 Project Overview

This project focuses on predicting monthly **U.S. inflation** using three critical macroeconomic variables from 2000 to 2023:

- 🏦 **Federal Funds Rate** – Indicator of monetary policy
- 📉 **Unemployment Rate** – Reflects labor market slack
- 💵 **M2 Money Supply** – Measures liquidity in the economy

All data was collected from the [Federal Reserve Economic Database (FRED)](https://fred.stlouisfed.org/), and a variety of regression models were applied to assess predictive performance.

---

## 📁 Repository Contents

| File | Description |
|------|-------------|
| `Report.pdf` | Final report with analysis, results, and policy implications |
| `US_Inflation _Prediction.ipynb` | Jupyter Notebook with all code, visualizations, and models |
| `CPIAUCSL.csv` | Consumer Price Index (CPI) data |
| `FEDFUNDS.csv` | Federal Funds Rate data |
| `M2SL.csv` | M2 Money Supply data |
| `UNRATE_CPIAUCSL_PC1.csv` | Merged dataset of Unemployment and CPI data |

---

## 🔍 Methodology

### 1. Data Preparation  
- Monthly data from 2000 to 2023  
- Cleaned and merged on timestamp  
- 277 observations  
- Handled missing values, assessed stationarity

### 2. Exploratory Data Analysis (EDA)  
- Time series plots, rolling averages  
- Correlation heatmap  
- Focus on structural shifts: 2008 crisis, COVID-19 impact

### 3. Modeling & Evaluation  
Models used:

| Model | MAE | MSE | R² |
|-------|-----|-----|----|
| Linear Regression | 1.573 | 3.530 | 0.068 |
| **Random Forest Regressor** | **0.319** | **0.230** | **0.939** |
| Decision Tree Regressor | 0.496 | 0.488 | 0.871 |

> **Best performing model:** Random Forest Regressor  
> **Top feature:** M2 Money Supply

---

## 📈 Forecast Example

Using the most recent data, predicted inflation for the next month:

- Linear Regression: `7.77%`  
- Random Forest: `10.09%`  
- Decision Tree: `9.84%`

---

## 🧠 Key Insights

- Inflation is positively affected by M2 growth and low interest rates.  
- Unemployment has a weaker or delayed influence.  
- Ensemble models capture complex, non-linear relationships better.  
- Results are useful for monetary policy, investment strategy, and macroeconomic forecasting.

---

## 🧩 Future Improvements

- Include exogenous shocks (oil, war, pandemics)  
- Use LSTM/GRU models for deep learning on time series  
- Apply SHAP for better interpretability of model decisions

---

## 🚀 How to Run

```bash
# Clone the repo
git clone https://github.com/<your-username>/us-inflation-prediction.git
cd us-inflation-prediction

# Install dependencies
pip install -r requirements.txt

# Launch the notebook
jupyter notebook "US_Inflation _Prediction.ipynb"
