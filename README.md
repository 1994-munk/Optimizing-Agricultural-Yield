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

## 📈 Animated Weather Trends

An animated GIF can display daily temperature and rainfall trends for a selected location. Generate the GIF using Python from your weather dataset (example provided below) and embed it here:

![Mombasa Weather](mombasa_weather.gif)

---

## ☀️ Weather Icon (Static SVG)

```html
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
```


🛠 Methodology

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

🔗 Tools and Resources

Python libraries: pandas, numpy, matplotlib, seaborn, plotly

Weather APIs: OpenWeatherMap
, NOAA

Agricultural datasets: Local Ministry of Agriculture, FAO

📌 Next Steps

Integrate live weather API feeds for real-time updates

Automate weekly weather summary GIF generation

Create interactive maps showing farm locations and rainfall overlays

Merge crop yield and weather data for predictive modeling

🧩 Python Example: Generate Animated Weather GIF
import pandas as pd
import matplotlib.pyplot as plt
from matplotlib.animation import FuncAnimation

# Load weather dataset
weather = pd.read_csv("weather_data.csv")  # Ensure it has date, location, temp, rainfall
mombasa = weather[weather['location'] == 'Mombasa']

fig, ax1 = plt.subplots(figsize=(6,4))
ax2 = ax1.twinx()

ax1.set_xlim(0, len(mombasa))
ax1.set_ylim(mombasa['temperature_c'].min()-2, mombasa['temperature_c'].max()+2)
ax2.set_ylim(0, mombasa['rainfall_mm'].max()+5)

def animate(i):
    ax1.clear()
    ax2.clear()
    ax1.plot(range(i), mombasa['temperature_c'].iloc[:i], color='orange', label='Temp (°C)')
    ax2.bar(range(i), mombasa['rainfall_mm'].iloc[:i], color='blue', alpha=0.3, label='Rainfall (mm)')
    ax1.set_ylabel('Temperature (°C)')
    ax2.set_ylabel('Rainfall (mm)')
    ax1.set_xlabel('Days')
    ax1.set_ylim(mombasa['temperature_c'].min()-2, mombasa['temperature_c'].max()+2)
    ax2.set_ylim(0, mombasa['rainfall_mm'].max()+5)
    ax1.legend(loc='upper left')
    ax2.legend(loc='upper right')

ani = FuncAnimation(fig, animate, frames=len(mombasa), interval=300)
ani.save('mombasa_weather.gif', writer='pillow')

This generates a GIF that animates temperature and rainfall trends for Mombasa. Replace the location for other regions as needed.

✅ Features of this README:

Dynamic-looking badges for temperature and rainfall

Real weather animation via GIF

Static weather SVG for visual representation

Clear methodology and next steps for analysis
