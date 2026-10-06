# real-time-weather-powerbi-dashboard
Interactive Real-Time Weather Forecast Dashboard built using Microsoft Power BI, DAX, Power Query, and Weather API data.
# 🌦️ Real-Time Weather Forecast Dashboard using Power BI

An interactive **Real-Time Weather Forecast Dashboard** built using **Microsoft Power BI** to visualize current weather conditions, 7-day forecasts, air quality, atmospheric indicators, and rainfall probabilities across multiple cities.

The dashboard combines weather API data with Power Query transformations, data modeling, DAX measures, and interactive Power BI visualizations to provide an intuitive view of environmental conditions.

---

## 📊 Dashboard Preview

![Weather Dashboard](Screenshots/dashboard.png)

---

## 🎯 Project Objective

The main objective of this project is to build a clear, accurate, and interactive weather-monitoring dashboard using Power BI.

The dashboard provides:

- Real-time weather information
- 7-day weather forecasts
- Air Quality Index (AQI) analysis
- Pollutant-level information
- Rain probability
- Sunrise and sunset timings
- Atmospheric indicators
- Interactive city selection

---

## ✨ Key Features

### 🌡️ Current Weather

Displays the current weather conditions for the selected city, including:

- Temperature
- Weather condition
- Humidity
- Wind speed
- Visibility
- Atmospheric pressure
- UV Index
- Precipitation

---

### 📅 7-Day Weather Forecast

Provides a short-term weather outlook with:

- Daily temperature predictions
- Weather conditions
- Weather icons
- Rain probability
- Temperature trends
- Avg Temp =AVERAGE(Forecast[Temp])

---

### 🌅 Sunrise & Sunset

Displays:

- Sunrise time
- Sunset time
- Daylight information
- SunriseFormatted = FORMAT([Sunrise], "hh:mm AM/PM")
---

### 🌬️ Atmospheric Indicators

The dashboard provides KPI-style indicators for:

- Humidity
- Wind Speed
- Visibility
- Pressure
- UV Index
- Precipitation

---

### 🌫️ Air Quality Analysis

The dashboard includes an Air Quality Index section with:

- AQI
- PM10
- PM2.5
- CO
- SO2
- NO2
- O3

AQI levels are categorized into:

- Good
- Moderate
- Poor

---

### 🌧️ Rain Probability

Visualizes the probability of rainfall for each day of the upcoming week.

This helps users understand potential rainy days and plan weather-dependent activities.
Rain % =AVERAGE(Weather[Rain_Probability])

---

## 🗂️ Dataset

The dashboard uses weather data obtained through a Weather API.

The dataset contains weather and environmental information for selected cities.

### Main Fields

| Field | Description |
|---|---|
| City_Name | Name of the selected city |
| Temperature | Current temperature in °C |
| Feels_Like | Perceived temperature |
| Weather_Condition | Current weather condition |
| Humidity | Humidity percentage |
| Wind_Speed | Wind speed in kph |
| Visibility | Visibility distance in km |
| Pressure | Atmospheric pressure |
| UV_Index | UV radiation level |
| Precipitation | Rainfall amount |
| Sunrise | Sunrise time |
| Sunset | Sunset time |
| Forecast_Temp_Day1-Day7 | Forecast temperature |
| Rain_Probability_Day1-Day7 | Rain probability |
| AQI | Air Quality Index |
| PM10 | PM10 pollutant level |
| PM2.5 | PM2.5 pollutant level |
| CO | Carbon monoxide level |
| SO2 | Sulfur dioxide level |
| NO2 | Nitrogen dioxide level |
| O3 | Ozone level |

---

## 🔄 Data Preparation

Data preparation was performed using **Power Query Editor** in Power BI.

The main steps included:

1. Loading data from Web / JSON / CSV sources
2. Extracting and expanding nested API data
3. Cleaning missing and inconsistent values
4. Standardizing text fields
5. Converting numerical fields to appropriate data types
6. Converting Unix timestamps into readable date/time formats
7. Expanding 7-day forecast data
8. Creating temperature categories
9. Categorizing AQI levels
10. Restructuring pollutant data
11. Validating weather and environmental values
12. Building relationships between tables
13. Removing unnecessary columns
14. Loading the final dataset into the Power BI model

---

## 🧮 DAX Measures

Some of the DAX measures used in the dashboard include:

### Temperature Category

```DAX
Temp Category =
IF(
    [Temperature] > 30,
    "Hot",
    IF(
        [Temperature] > 20,
        "Warm",
        "Cool"
    )
)
```
---
### 🛠️ Technologies & Tools
- Microsoft Power BI
- Power Query
- DAX
- Weather API
- Data Modeling
- Data Visualization
- Custom Power BI Visuals

---

### 📈 Dashboard Components
The dashboard contains:
- Current Weather Card
- 7-Day Forecast
- Sunrise & Sunset Panel
- Atmospheric KPI Indicators
- Air Quality Index Gauge
- Pollutant Indicators
- Rain Probability Chart
- Interactive City Selector
- Hover Tooltips
- Drill-through functionality
- Dynamic Forecast Updates

---
