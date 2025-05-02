---
name: Weather Modeling for Urbana 
tools: [Python]
image: assets/pngs/UIUC.png
description: This will be a data analysis of Urbana weather. (2023)

custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Introduction 

The purpose of this report is to reliably predict when to go outdoors during Autumn. This will involve creating a model to predict the minimum daily temperature to find out if it will be too cold to go outside. This data is obtained using historical weather data from the Historical Weather API of Open-Meteo. The data will include the minimum air temperature at 2 meters above ground for the day, year, month, day and day of the year.

Living in Urbana, this information is also pretty helpful for me.

## Data

This is the data after being cleaned. 

<img title="Weather data" alt="weather data" src="/assets/pngs/weather_data.png">

## Visualization

The different pitch types are visualized in this graph. 

<img title="Weather graph" alt="model graph" src="/assets/pngs/weather_visualization.png">