![Python](https://img.shields.io/badge/Python-3.10-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![License](https://img.shields.io/badge/License-MIT-yellow)

# 🌍 Global Air Quality Analysis

## 📌 Project Overview

This project analyzes global air pollution data to uncover patterns, identify the most polluted regions, and determine which pollutants contribute most to overall air quality index (AQI).

The analysis includes **data cleaning, exploratory data analysis (EDA), visualization, and correlation analysis** using Python.

---

## 🎯 Objectives

* Analyze air quality across countries and cities
* Identify the most polluted regions
* Determine key pollutants influencing AQI
* Visualize pollution trends and relationships
* Build insights useful for environmental decision-making

---

## 📂 Dataset

* Source: Global Air Pollution Dataset
* Format: CSV
* Records: 23,000+ entries
* Features:

  * Country & city information
  * Overall AQI
  * Pollutant-specific AQI values (CO, NO₂, Ozone, PM2.5)

---

## 🛠️ Technologies Used

* Python 🐍
* Jupyter Lab
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

---

## 🔍 Data Cleaning

* Handled missing values in `country_name`
* Checked and removed duplicate records
* Validated AQI values for inconsistencies
* Ensured correct data types

---

## 📊 Exploratory Data Analysis

### Key Questions Answered:

* Which countries have the highest pollution levels?
* Which cities are the most polluted?
* How do different pollutants relate to overall AQI?

---

## 📈 Visualizations

### 📌 Top 10 Most Polluted Cities

![Top Cities](images/average_aqi_by_country.png)

### 📌 Average AQI by Country

![AQI by Country](images/average_aqi_by_country.png)

### 📌 Pollutant Relationships

![Scatter Plot](images/co_vs_no2_aqi_relationship.png)

---

## 🔍 Correlation Analysis

To understand pollutant impact on air quality:

```python
correlation = df[['co_aqi_value', 'ozone_aqi_value', 'no2_aqi_value', 'pm2.5_aqi_value']].corrwith(df['aqi_value'])
strongest = correlation.idxmax()
```

### Key Insight:

* The pollutant with the highest correlation has the strongest influence on overall AQI
* This helps identify the primary driver of pollution

---

## 🧠 Key Insights

* Certain countries consistently show higher AQI levels
* Urban cities tend to have worse air quality
* One pollutant (e.g., PM2.5) plays a dominant role in AQI
* Strong correlations exist between pollutant levels and AQI

---

## 🤖 Machine Learning

A simple regression model was built to predict AQI using pollutant values.

### Model Evaluation:

* Mean Absolute Error (MAE)
* Mean Square Error (MSE)
* R² Score

---

## 📁 Project Structure

```
air-quality-analysis/
│
├── air_quality_analysis.ipynb
├── global_air_pollution_data.csv
├── images/
├── README.md
└── requirements.txt
```

---

## 🚀 How to Run the Project

1. Clone the repository:

```bash
git clone https://github.com/Chirunga-Chiro/global_air_pollution_analysis
```

2. Navigate into the folder:

```bash
cd global_air_pollution_analysis
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Launch Jupyter Lab:

```bash
jupyter-lab
```

---

## 📌 Future Improvements

* Add time-series analysis (if timestamp data is available)
* Deploy as a dashboard (Streamlit / Power BI)
* Improve machine learning model performance
* Integrate real-time air quality APIs

---

## 👤 Author

**Chirunga Chiro**
Data Scientist 🚀

---

## ⭐ If you found this project useful

Give it a ⭐ on GitHub!
