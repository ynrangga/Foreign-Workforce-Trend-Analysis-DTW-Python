# 📊 Foreign Workforce Trend Analysis using Dynamic Time Warping (DTW)

## 📌 Project Overview
This project analyzes **time-series trends of foreign workers (Tenaga Kerja Asing / TKA)** in Central Java Province from 2014 to 2024 using **Exploratory Data Analysis (EDA)** and **Dynamic Time Warping (DTW)**.

The main **focus** is to identify **similarity patterns across nationalities** based on their workforce trends over time, even when temporal shifts or irregular fluctuations occur. DTW is applied to capture non-linear temporal similarities that traditional distance measures fail to detect.

## 🎯 Objectives
- Explore long-term trends of foreign workforce distribution by nationality
- Visualize workforce dynamics before, during, and after the COVID-19 period
- Identify countries with similar temporal workforce patterns using DTW
- Cluster nationalities based on time-series similarity and validate results statistically

## 📂 Dataset Information
- Source: Badan Pusat Statistik (BPS) Provinsi Jawa Tengah
- Period: 2014 – 2024
- Granularity: Yearly time series
- Key Attributes:
  - Nationality
  - Year
  - Number of Foreign Workers
  - Total Workforce (aggregate)
This dataset reflects official workforce permits for foreign nationals engaged in independent business activities.

## 🛠 Tools & Technologies
- Python
- Google Colab
- Library Python
  - pandas, numpy
  - matplotlib, seaborn
  - scipy
- Dynamic Time Warping (DTW)

## 📊 Analysis Performed
### 1️⃣ Exploratory Data Analysis (EDA)
- Yearly trend analysis of total foreign workforce
- Top 5 nationalities with the highest workforce contribution
- Nationality categorization based on workforce volume (low, medium, high)
- Comparative trend visualization across countries
- Identification of extreme fluctuations during pandemic and post-pandemic periods
### 2️⃣ Time Series Similarity Analysis
- Application of Dynamic Time Warping (DTW) to measure similarity between nationality-based time series
- Hierarchical clustering using Complete Linkage
- Visualization of similarity structure through dendrograms
### 3️⃣ Cluster Validation
- Evaluation of cluster quality using Silhouette Score
- Optimal clustering achieved with 3 clusters
- Interpretation of cluster characteristics based on trend behavior

## 🔍 Key Quantitative Insights
- Workforce volatility is extreme, with total foreign workers increasing from 12,193 (2021) to 138,662 (2022) (>10× YoY growth), indicating strong post-pandemic recovery effects.
- China (PRC) dominates workforce contribution, accumulating 79,162 workers (2014–2024) and accounting for 44.3% of total foreign workers in 2024, making it a statistical outlier.
- DTW-based hierarchical clustering (Complete Linkage) identifies 3 optimal clusters, validated by the highest Silhouette Score of 0.719 (k = 3).
### 📈 Clustering Results (DTW-Based)
| Cluster   | Characteristics                                            |
| --------- | ---------------------------------------------------------- |
| Cluster 1 | Low-volume, stable workforce trends (14 nationalities)     |
| Cluster 2 | Moderate-to-high, fluctuating trends (Japan, Korea, India) |
| Cluster 3 | Extreme, dominant trend (China – PRC)                      |

Optimal cluster count determined using Silhouette Score (highest at k = 3).
