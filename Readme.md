# 🌍 Air Quality Time Series Forecasting

This project focuses on forecasting **PM2.5 air quality readings** using a variety of **time series modeling techniques**, progressing from data wrangling to advanced ARMA forecasting.  
Each stage introduces new analytical and modeling concepts, forming a complete end-to-end time series pipeline.

---

## 📄 Overview

Air pollution, especially **PM2.5 (Particulate Matter < 2.5µm)**, is a key indicator of environmental health.  
This project aims to predict PM2.5 concentrations over time using data collected from the **Nairobi Air Quality Database**.

We start by **cleaning and transforming** data, then move through **Linear Regression**, **Autoregressive**, and **ARMA** models to improve forecasting accuracy.

---

## 🧮 Dataset

- **Source:**[open.africa/dataset](https://open.africa/dataset) open.Africa database   
- **Location:** Nairobi, Kenya  
- **Features:** Timestamped PM2.5 air quality readings (hourly frequency)  
- **Cleaning:** Missing values handled via forward fill; timezone localized to `Africa/Nairobi`

---

## ⚙️ Workflow

1. **Data Extraction & Wrangling:**  
   Downloaded the data in CSV form  and transformed raw air quality data into a clean, structured format.

2. **Feature Engineering:**  
   Created lag-based and time-derived features to capture temporal patterns and dependencies.

3. **Modeling & Forecasting:**  
   Built multiple models — Linear Regression, Autoregressive (AR), and ARMA — to progressively enhance prediction accuracy.

4. **Evaluation & Visualization:**  
   Compared model outputs using **MAE** and plotted actual vs. predicted PM2.5 levels for interpretability.

---

## 🧩 Models Used


### 📈 Linear Regression with Time Series Data  
📘 Notebook: `Linear_regression.ipynb`  
- Built a **Linear Regression model** on time-based features.  
- Modeled PM2.5 as a function of historical timestamps.  
- Served as a baseline model for comparison with time-dependent methods.

---

### 🔁 Autoregressive (AR) Model  
📘 Notebook: `AutoReg.ipynb`  
- Trained an **AR(p)** model to predict PM2.5 based on previous hourly readings.  
- Used **lag order = 26**, chosen based on lowest Mean Absolute Error (MAE).  
- Implemented **walk-forward validation** to simulate real-time forecasting.

---

### ⚙️ ARMA Model & Hyperparameter Tuning  
📘 Notebook: `ARMA model.ipynb`  
- Combined **autoregressive (AR)** and **moving average (MA)** terms into an **ARMA(p, q)** model.  
- Tuned parameters `p` and `q` via grid search using MAE-based heatmaps.  
- Identified the optimal configuration that balanced **accuracy** and **computational efficiency**.

---

## 📊 Evaluation

- **Metric Used:** Mean Absolute Error (MAE)  
- Compared model predictions on both training and test data.  
- Best performance achieved by the **ARMA(8, 0, 1)** configuration during walk-forward validation.  
- Evaluation confirmed model stability and ability to adapt to real-time sequences.

---

## 📈 Visualization

- Used **Plotly Express** to plot **actual vs. predicted PM2.5** readings.  
- Created interactive time series charts to highlight model performance.  
- Visualizations helped identify periods where predictions aligned or deviated from observed data.

---

## 🏁 Results and Insights

- Cleaned and modeled over **one month** of hourly air quality readings.  
- Demonstrated improvements from **baseline (Linear Regression)** to **AR/ARMA models**.  
- **Walk-forward validation** proved the model’s adaptability in sequential forecasting.  
- Interactive visualizations made trend analysis intuitive and engaging.

---

## 💡 Conclusion

This project demonstrates a **complete time series forecasting workflow** — from **data wrangling** to **predictive modeling and visualization**.  
It highlights core skills in:

- Time series analysis  
- Model evaluation and tuning  
- Real-world data handling
- Interactive visualization using Plotly  

The techniques and methodology here are directly applicable to **data analytics**, **environmental monitoring**, and **predictive modeling** projects.

---

## 🧠 Tech Stack

- **Languages:** Python  
- **Libraries:** Pandas, Statsmodels, Scikit-learn, Plotly, Seaborn, Matplotlib  
- **Tools:** Jupyter Notebook  

---

## ✨ Author
**Pushkin Kumar**  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/pushkin-kumar)
_Data Analyst | Data Engineer_  
Passionate about building modern data pipelines and predictive models.
