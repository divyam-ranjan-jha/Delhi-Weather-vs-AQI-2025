# Delhi-Weather-vs-AQI-2025
Data Analysis on Dependance of AQI on Weather conditions


# Winter AQI–Weather Relationship Analysis (India)

## Overview
This project studies the relationship between **PM2.5 (air pollution)** and **meteorological parameters** during the **winter period (15 Oct – 23 Dec 2025)** using openly available APIs.  
The objective is **explanatory analysis**, not prediction: to understand *which weather factors matter* for winter air quality and *why*.

## Motivation
Winter months in North India experience severe air pollution episodes driven by:
- Thermal inversion
- Atmospheric stagnation
- Reduced dispersion

To avoid seasonal confounding, the analysis is **restricted to winter only** and uses **lagged weather variables** where physically meaningful.

## Data Sources
- **Air Quality:** Open-Meteo Air Quality API (PM2.5, hourly → daily)
- **Weather:** Open-Meteo Weather API  
  Variables used:
  - Temperature (2m)
  - Relative Humidity (2m)
  - Wind Speed (10m)
  - Precipitation
  - Mean Sea Level Pressure

All data are freely accessible and reproducible.

## Data Processing
1. Hourly data aggregated to **daily means**
2. Winter date filtering applied
3. Feature engineering:
   - Lagged variables (t−1 day)
   - Rain dummy (0/1)
   - Weekend indicator
4. Missing values dropped only where required (due to lags)

## Methodology
### Exploratory Analysis
- Correlation analysis (same-day and lagged)
- Winter-specific interpretation

### Modeling Approach
- **Ordinary Least Squares (OLS) Regression**
- Rationale:
  - Focus on interpretability
  - Quantify direction and magnitude of effects
  - Standard method in environmental science

### Core Regression Model
PM2.5(t) ~  
- Wind(t−1)  
- Rain(t−1)  
- Temperature(t−1)  
- Humidity(t)  
- Pressure(t)

## Key Results
- **Temperature (lagged)**: Strong, negative, statistically significant  
  → Confirms thermal inversion & stagnation hypothesis
- **Relative Humidity**: Significant negative effect in winter
- **Wind & Rain**: Weak or insignificant lagged effects
- **Model explanatory power**: ~22–28% (Adjusted R²), typical for environmental data

## Interpretation
Winter PM2.5 levels are primarily governed by **atmospheric stability**, not short-term dispersion mechanisms.  
Meteorological variables explain a meaningful but partial share of pollution variability, highlighting the role of emissions and regional transport not captured in this study.

## Limitations
- No emissions data included
- Daily aggregation smooths extreme events
- Autocorrelation present (time-series nature)

## Future Scope
- ARIMAX / dynamic regression with PM2.5 lag
- City-to-city comparison
- Inclusion of boundary layer height
- Policy-period analysis (e.g., GRAP days)

## Tools Used
- Python
- pandas, statsmodels
- Open-Meteo APIs
- Jupyter Notebook

## Author
Divyam Ranjan Jha  
(IIT Delhi)
