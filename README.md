Here's a **GitHub-ready README** (paragraph + point-wise style) for your Wind Turbine Anomaly Detection and Health Monitoring project:


# 🌬️ Wind Turbine Health Monitoring with Anomaly Detection and SHAP Explainability

This project performs **health monitoring of wind turbines** using SCADA data. It applies machine learning techniques to detect anomalies, estimate equipment degradation, calculate health scores, and provide model interpretability using SHAP (SHapley Additive exPlanations). The analysis is visualized through various plots to offer insights into turbine behavior over time.



## 🔍 Project Overview

* **Data Source**: A CSV file containing time-stamped turbine parameters such as power output, wind speed, and theoretical power.
* **Goal**: Detect abnormal behavior and performance degradation in wind turbines, and assign a dynamic health score over time.
* **Tech Stack**: Python, Pandas, Scikit-learn, SHAP, Matplotlib, Seaborn.

---

## 🧠 Steps Performed

### 1. **Data Preprocessing**

* Load CSV and convert `'Date/Time'` to datetime format.
* Set the timestamp as the DataFrame index.
* Select key numerical features:

  * `LV ActivePower (kW)`
  * `Wind Speed (m/s)`
  * `Theoretical_Power_Curve (KWh)`
  * `Wind Direction (°)`

### 2. **Feature Scaling**

* Standardize features using `StandardScaler` for effective modeling.

### 3. **Anomaly Detection**

* Use **Isolation Forest** to flag unusual patterns in turbine behavior.
* Detect outliers based on multivariate relationships in the data.

### 4. **Degradation Analysis**

* Use gradients of power and wind speed to calculate degradation indicators.
* Fit a **linear regression model** to estimate impact of degradation on power output.

### 5. **Health Score Calculation**

* Calculate a **Health Score (0-100)** based on:

  * Anomaly score (from Isolation Forest)
  * Degradation trend (from regression model)

### 6. **SHAP Explainability**

* Use SHAP to understand the contribution of each feature to the anomaly scores.
* Generate summary and beeswarm plots for interpretability.

---

## 📊 Visualizations

* 📈 Health Score Over Time
* 🔴 Anomaly Scatter Plot (Power vs Wind Speed)
* ⚠️ Degradation Score Over Time
* 📉 Anomaly Score Distribution
* 🧬 SHAP Summary & Beeswarm Plots
* 🧿 Pairplot of features split by Anomaly status

---

## 💾 Output

* CSV file: `wind_turbine_health_scores_with_explainability.csv`
  Contains original features, anomaly flags, degradation scores, and health scores.

---

## 📌 Requirements

```bash
pip install pandas numpy matplotlib seaborn shap scikit-learn
```

---

## 🧠 Future Improvements

* Use time series models (e.g., LSTM) for more dynamic pattern recognition.
* Implement multivariate anomaly scoring with advanced models like Autoencoders.
* Integrate real-time dashboard for monitoring.
* Train on larger datasets from multiple turbines for generalization.

---

## 📄 License

This project is for research and educational use only. All rights reserved to the original data owner.

---

Let me know if you'd like this in `.md` file format or want additional sections like badges, demo video, or usage instructions.
