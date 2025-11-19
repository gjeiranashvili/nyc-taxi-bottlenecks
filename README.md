# NYC Taxi Demand Bottlenecks: Exploratory Analysis of Spatiotemporal Ride Patterns 🚖📊

## Project Summary

This repository presents an exploratory data analysis (EDA) of taxi demand bottlenecks in New York City using a public dataset of yellow taxi trips. The aim is to uncover spatial and temporal concentration patterns in taxi pickups and drop-offs, identify latent demand surges, and offer groundwork for downstream applications such as predictive dispatching, congestion mapping, and urban transport planning.

## Motivation

Urban mobility data offers a rich lens into the behavioral pulse of a city. Understanding how taxi demand fluctuates over time and space in a complex environment like NYC is essential for:
- **Reducing inefficiencies** in driver allocation and wait times
- **Informing smart city infrastructure** (e.g., curb space, dynamic pricing)
- **Improving urban planning** in response to crowding and congestion

This notebook explores taxi usage patterns at the granular level to detect where and when demand bottlenecks emerge, and sets the stage for causal modeling and predictive analytics.

---

## Data

- **Source:** NYC Taxi and Limousine Commission (TLC) Public Datasets  
- **Subset used:** Yellow taxi trip data (`pickup_datetime`, `dropoff_datetime`, `pickup_longitude`, `pickup_latitude`, etc.)
- **Size:** Millions of observations aggregated for efficient spatiotemporal analysis

---

## Analytical Highlights

- **Time Series Aggregation:** Hourly taxi pickups across different days and boroughs
- **Peak Demand Detection:** Identification of rush hour clusters and weekend surges
- **Geospatial Mapping:** Spatial clustering of pickup hotspots using coordinate data
- **Bottleneck Zones:** Identification of high-density zones (e.g., Midtown, JFK, Financial District)
- **Seasonal Insights:** Exploratory plots of cyclical patterns and anomalies

---

## Tools and Libraries

- Python (Jupyter Notebook)
- `pandas`, `numpy`
- `matplotlib`, `seaborn`
- `datetime`, `geopandas` *(optionally extendable for mapping)*

---

## Key Findings (Preliminary)

- **Weekday vs Weekend**: Distinct shift in temporal peak hours and spatial hotspots
- **Rush Hour Compression**: Narrow window of extremely high demand in weekdays (8–10 AM, 5–7 PM)
- **Persistent Bottlenecks**: Locations like Penn Station and JFK Airport consistently show elevated demand regardless of hour

---

## Next Steps

- **Predictive Modeling**: Train a time series model (e.g., SARIMA, Prophet) to forecast hourly demand  
- **Spatial Clustering**: Apply DBSCAN/KMeans for better geospatial bottleneck classification  
- **Integration**: Merge with traffic, weather, and public transit datasets to assess systemic interactions  
- **Policy Simulation**: Evaluate policy interventions (e.g., dynamic pricing or driver re-routing)

---

## Folder Structure

```text
📁 nyc-taxi-bottlenecks/
├── nyc_taxi_demand_bottlenecks.ipynb   # Main analysis notebook
├── README.md                           # Project overview
└── data/                               # (optional) Preprocessed data files
