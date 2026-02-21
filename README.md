# 🌾 My Agricultural Evaluation Project (Live Weather Edition)

Hey! This project is my exploration into how crops perform in different farms, how soil affects growth, and most importantly… how the **weather impacts everything**. I’m combining farm data with weather trends to see patterns, make predictions, and basically geek out on agriculture. 🌱🌦️  

---

## 📂 What I’m Using

### 1. Crop & Farm Data
- **Where it’s from:** Local surveys & gov datasets  
- **Format:** CSV / Excel  
- **Columns I’m looking at:**
date | location | temperature_c | rainfall_mm | humidity_percent | wind_speed_kmh
- I use this to see how **rainfall, temperature, and humidity affect crops**.

---

## 🌦️ Live Weather Summary (Shields Style)

 
![Mombasa Rainfall](https://img.shields.io/badge/Rainfall-120mm-blue)  
![Mombasa Temp](https://img.shields.io/badge/Temperature-28°C-orange)  

> I plan to hook this up with a GitHub Action so these numbers update automatically every day.  

---



## ☀️ Tiny SVG Weather Fun

<svg width="50" height="50" xmlns="http://www.w3.org/2000/svg">
  <circle cx="25" cy="25" r="12" fill="yellow"/>
  <line x1="25" y1="0" x2="25" y2="10" stroke="orange" stroke-width="2"/>
  <line x1="25" y1="40" x2="25" y2="50" stroke="orange" stroke-width="2"/>
  <line x1="0" y1="25" x2="10" y2="25" stroke="orange" stroke-width="2"/>
  <line x1="40" y1="25" x2="50" y2="25" stroke="orange" stroke-width="2"/>
  <line x1="5" y1="5" x2="12" y2="12" stroke="orange" stroke-width="2"/>
  <line x1="38" y1="38" x2="45" y2="45" stroke="orange" stroke-width="2"/>
  <line x1="5" y1="45" x2="12" y2="38" stroke="orange" stroke-width="2"/>
  <line x1="38" y1="12" x2="45" y2="5" stroke="orange" stroke-width="2"/>
</svg>


🛠️ How I Work

Cleaning the data

Fill missing values

Standardize dates & location names

Exploring the data (EDA)

Rainfall vs crop yield

Soil pH vs productivity

Seasonal trends

Evaluation Metrics

Yield per hectare

Rainfall efficiency

Temperature stress periods

Optional ML fun

Predict crop yields based on soil + weather

Flag risky periods for certain crops

🔗 Tools & Resources

Python libraries: pandas, numpy, matplotlib, seaborn, plotly

Weather APIs: OpenWeatherMap
, NOAA

Agriculture Data: Local Ministry of Agriculture, FAO

📌 Next Steps in My Project

Hook up live weather API feeds

Auto-generate weekly weather summary GIFs

Add interactive maps with rainfall overlays

Merge weather + crop yield data for predictive modeling
