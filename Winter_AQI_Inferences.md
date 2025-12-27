# Winter AQI–Weather Inferences (Complete)

This document consolidates **all key inferences and interpretations** derived throughout the AQI–weather analysis discussion and modeling process.  
Scope: **Winter period (15 Oct – 23 Dec 2025)**, daily data, PM2.5 focus.

---

## 1️⃣ Biggest Driver: Temperature vs PM2.5 (≈ −0.4 to −0.5)

### What the numbers say
- Moderate to strong **negative association** between temperature and PM2.5.
- Consistent across:
  - Correlation analysis
  - Lagged correlation
  - OLS regression (same-day and lagged)

### What it actually means
- **Lower temperatures → higher PM2.5**
- Classic winter pollution mechanism:
  - Cold air → **thermal inversion**
  - Reduced vertical mixing
  - Pollutants trapped near the surface

### Key insight
> PM2.5 concentrations rise significantly during lower-temperature periods, indicating seasonal accumulation effects rather than emission spikes alone.

📌 **Interview-ready angle**  
> “This suggests PM2.5 variation in winter is largely seasonal and meteorology-driven, not random.”

---

## 2️⃣ Pressure Is Silently Important (Indirect Effect)

### Observations
- Pressure–PM2.5 direct correlation: weak to moderate
- **Pressure ↔ Temperature:** strong negative correlation

### Real-world logic
- High-pressure systems → stable air
- Stable air → poor dispersion
- Combined effect:
  - **High pressure → low temperature → high PM2.5**

### Insight
> Elevated PM2.5 levels coincide with high-pressure, low-temperature conditions, reinforcing the role of atmospheric stability in pollution buildup.

📌 Pressure’s role is **structural**, not standalone — this is why it often appears insignificant in multivariate regression.

---

## 3️⃣ Wind Speed Results Are Counter-Intuitive (and That’s OK)

### What the data shows
- PM2.5 vs mean wind: weak positive
- PM2.5 vs max wind: weak positive
- Lagged wind vs PM2.5: positive but unstable

### Why this happens in real winter data
- Wind often increases **after** pollution has built up
- Possible **regional transport** of polluted air
- Shallow winter boundary layer → poor vertical dispersion
- Mean wind ignores **direction, duration, and timing**
- Seasonal confounding (winter winds ≠ summer winds)

### Correct way to phrase it
> Wind speed alone does not show a clear dispersive effect on PM2.5, suggesting that timing, direction, and seasonal context matter more than raw wind magnitude.

📌 **Important**  
Do **NOT** say “wind increases pollution.”  
Say:
> “Wind speed alone is insufficient to explain PM2.5 variation.”

This reflects mature analysis.

---

## 4️⃣ Rainfall Does What It Should — Briefly

### Observations
- Precipitation vs PM2.5: weak to moderate **negative** correlation
- Rain lag (t−1) vs PM2.5: very weak

### Physical explanation
- Wet deposition removes particles
- But the effect is **immediate**, not persistent

Also note:
- Rainfall ↔ Humidity: positive correlation
- High humidity ≠ clean air

### Insight
> While high humidity alone does not reduce PM2.5, actual precipitation events contribute to measurable pollution reduction through wet scavenging.

---

## 5️⃣ Humidity Is Mostly an Indirect Player

### What the data says
- Weak direct correlation with PM2.5
- Significant in some regressions, but secondary

### Role of humidity
- Acts as a **proxy variable**
- Interacts with:
  - Temperature
  - Fog/drizzle conditions
  - Rainfall

### Insight
> Relative humidity shows limited direct association with PM2.5, indicating it influences pollution indirectly through precipitation, boundary-layer conditions, and seasonal effects.

---

## 6️⃣ One High-Quality Combined Insight (Core Takeaway)

Putting all meteorological variables together:

> PM2.5 levels in winter are driven primarily by **atmospheric stability**, not by individual weather variables in isolation.  
Low temperature, high pressure, and limited dispersion conditions contribute more to pollution buildup than short-term wind or humidity changes.

📌 This is a **senior-level inference**, suitable for reports, interviews, and discussions.

---

## 7️⃣ Winter AQI–Weather Lag Analysis (15 Oct – 23 Dec 2025)

### Lagged Correlation Summary (t vs t−1)

| Variable (lag-1) | Association with PM2.5 |
|------------------|------------------------|
| Wind speed       | **+0.20** |
| Rain             | **−0.10** |
| Temperature      | **−0.39** |

---

### Lag-Specific Inferences

#### 1. Temperature (lag-1): Dominant driver
- Colder conditions yesterday → higher PM2.5 today
- Confirms **thermal inversion persistence**
- Strongest and most stable lagged effect

#### 2. Rain (lag-1): Short-lived impact
- Weak negative association
- Washout effect is mostly **same-day**
- Lagged influence fades quickly

#### 3. Wind (lag-1): Mixed, context-dependent
- Positive association does not imply causation
- Reflects:
  - Regional pollutant transport
  - Limited winter dispersion
- Wind plays a **dual role**: dispersion vs transport

---

## 8️⃣ Inter-Weather Relationships (Why Regression Was Needed)

- **Wind ↔ Temperature:** Negative correlation  
  → creates confounding in simple correlations
- **Wind ↔ Rain:** Positive correlation  
  → rain effects weaken in multivariate models

📌 This justifies the use of **OLS regression** to isolate independent effects.

---

## 9️⃣ Regression-Level Conclusions (Winter-only)

From OLS (same-day and lagged models):

- **Temperature (same-day & lag-1):** Negative, statistically significant
- **Relative Humidity:** Significant but secondary
- **Wind & Rain:** Weak or insignificant after controls
- **Pressure:** Indirect, absorbed via temperature
- **Model explanatory power:** ~22–33% (Adjusted R²)

This is **normal and acceptable** for environmental systems.

---

## 🔚 Final Winter-Specific Conclusion

> During winter, PM2.5 variability is primarily governed by atmospheric stability. Lower temperatures and associated high-pressure conditions promote pollutant accumulation, while wind and rainfall exhibit weaker and context-dependent effects due to limited dispersion and regional transport.

---

## 📌 Important Framing Note
- Results explain **meteorological modulation**, not emissions
- Findings should be interpreted as **drivers of accumulation**, not causes of emissions
- Lower R² does not indicate poor modeling — it reflects system complexity

---

**End of Inference Document**
