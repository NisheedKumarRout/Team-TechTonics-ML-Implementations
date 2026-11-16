# Review 1: Citi Bike Bicycle Availability & Demand Prediction

## 📋 Problem Statement
> **"Develop an ML system that predicts the number of bicycles likely to be available at different bike-sharing stations. The model can use historical usage, time, weather, nearby transport stations, and commuting patterns."**

---

## 🎯 Project Overview
Bike-sharing systems are critical municipal transit assets that suffer from severe dynamic supply-demand imbalances. During morning and evening peak commute hours, popular stations near commercial hubs or transit terminals frequently experience either:
- **Bike Stockouts (Zero Availability):** Depriving commuters of transport.
- **Full Docks (Zero Influx Capacity):** Preventing riders from docking and returning bikes.

This project delivers an end-to-end data analysis and predictive modeling foundation utilizing the **full 2014 New York City Citi Bike dataset**, encompassing **8,081,216 ride transactions** across all 12 calendar months.

---

## 🔬 Core Methodology & Key Deliverables

1. **Comprehensive Statistical Profiling**:
   - **Central Tendency & Spread**: Mean ($\bar{x}$), Median ($Q_2$), Standard Deviation ($s$), Interquartile Range (IQR).
   - **Granular Quantiles & Percentiles**: Robust 1st to 99.9th percentile profiling to identify anomalous trips and outlier rides.
   - **Distribution Shape**: Skewness (asymmetry) and Kurtosis (tail-heaviness) analysis for trip duration distributions.

2. **Temporal & Commuting Pattern Analysis**:
   - Hourly surge curves distinguishing weekday commuter peaks (8:00–9:00 AM, 5:00–6:30 PM) from weekend recreational patterns.
   - Seasonal trend decomposition across winter troughs and summer peaks.
   - Day-of-week demand variance and subscriber vs. one-time customer behavior.

3. **Spatial & Station Availability Dynamics**:
   - High-volume station identification (e.g., Grand Central, Penn Station, 8th Ave & W 31st St).
   - Net-flow calculation: Station-level influx vs. outflow balance tracking real-time bicycle surpluses and deficits.
   - Geographic clustering of station hubs and route popularity.

4. **Environmental & External Factors**:
   - Weather condition impact on ride frequency and trip duration.
   - Rebalancing necessity estimation based on turnover velocity.

---

## 📁 Implementation File
- **Notebook**: [`citibike_eda_2014.ipynb`](citibike_eda_2014.ipynb)
