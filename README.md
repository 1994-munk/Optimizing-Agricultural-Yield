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

```html
<svg width="200" height="100">
  <circle cx="50" cy="50" r="20" fill="yellow">
    <animate attributeName="cx" from="50" to="150" dur="5s" repeatCount="indefinite" />
  </circle>
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
