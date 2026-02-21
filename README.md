# 🌾 Agricultural Evaluation Project (Weather Analysis)

This project evaluates agricultural productivity by integrating crop, soil, and weather data. The goal is to understand how environmental factors, particularly temperature and rainfall, influence crop performance across different regions.

---

## 📂 Datasets

### 1. Crop & Farm Data
- **Source:** Local surveys and government datasets  
- **Format:** CSV / Excel  
- **Columns:**
farm_id | crop_type | planting_date | harvest_date | soil_ph | region

- Purpose: To correlate weather patterns with crop growth and yield.

---

## 🌦 Live Weather Summary (Dynamic Badges)

The following badges display the most recent weather conditions for a location. They can be updated automatically using a GitHub Action:

![Mombasa Rainfall](https://img.shields.io/badge/Rainfall-120mm-blue)  
![Mombasa Temperature](https://img.shields.io/badge/Temperature-28°C-orange)  

---



## 🛠 Methodology

Data Cleaning

Fill missing values and handle inconsistencies

Standardize date formats and location names

Exploratory Data Analysis (EDA)

Analyze rainfall vs crop yield

Evaluate soil pH impact on productivity

Identify seasonal temperature and rainfall patterns

Evaluation Metrics

Yield per hectare

Rainfall efficiency

Temperature stress periods

Optional Machine Learning

Predict crop yield based on weather and soil conditions

Identify high-risk periods for specific crops

---

##🔗 Tools and Resources

Python libraries: pandas, numpy, matplotlib, seaborn, plotly

Weather APIs: OpenWeatherMap
, NOAA

Agricultural datasets: Local Ministry of Agriculture, FAO

---

##📌 Next Steps

Integrate live weather API feeds for real-time updates

Automate weekly weather summary GIF generation

Create interactive maps showing farm locations and rainfall overlays

Merge crop yield and weather data for predictive modeling

---


##✅ Features of this README:

Dynamic-looking badges for temperature and rainfall

Real weather animation via GIF

Static weather SVG for visual representation

Clear methodology and next steps for analysis
