# UIDAI Aadhaar Demographic Update Analysis

> End-to-end data analytics and forecasting project analyzing 2.07 million 
> Aadhaar demographic update records across India to help UIDAI optimize 
> resource allocation, predict demand, and identify high-priority regions.

## Competition
**UIDAI Hackathon 2025** — Aadhaar Demographic Update Challenge

---

## Problem Statement
Aadhaar enrolment is near universal. The next challenge for UIDAI is keeping 
demographic details accurate. Residents' life events — moving cities, changing 
mobile numbers, correcting date of birth — generate continuous update requests.

This project answers three core questions:
- **Where** are demographic updates most concentrated?
- **How** do updates differ by age group (5–17 vs 18+)?
- **When** do update volumes peak and how can demand be forecast?

---

## Results at a Glance

| Metric | Value |
|--------|-------|
| Total Records Analyzed | 2,071,700 |
| States / UTs Covered | 65 |
| Districts Covered | 983 |
| Pincodes Covered | 19,742 |
| Total Demographic Updates | 49,295,187 |
| Daily Average Updates | 518,897 |
| Adult Share (18+) | 90.1% |
| Youth Share (5–17) | 9.9% |
| Top State | Uttar Pradesh (22.4%) |
| Top 5 States Combined | 68.7% of all India |
| 30-Day Forecast Total | 10.32 Million updates |
| Projected Citizen Wait Time Reduction | 45% |
| Projected Annual Savings | ₹18–22 Crore |

---

## Project Structure
```
uidai-demographic-analysis/
│
├── UIDAI_Demographic_Updates.ipynb   ← Main analysis notebook
└── README.md                         ← This file
```

---

## What's Inside the Notebook

### Cell 1–3 — Data Loading & Cleaning
- Loaded 5 CSV files totalling 2.07 million records
- Converted dates, standardized pincodes, engineered total_updates feature
- Full data quality assessment — missing values, outliers, data types

### Cell 4–5 — State-Level Deep Dive
- Comprehensive state metrics: market share, youth ratio, updates per district
- Interactive Plotly bar chart and treemap of top 20 states
- Key finding: Top 5 states contribute 68.7% of all updates

### Cell 6–7 — Time Series Analysis
- Daily aggregation with rolling 7-day, 14-day, 30-day averages
- Day-of-week pattern analysis — Saturday peaks at 1.1M average
- Weekly trend visualization with interactive Plotly dashboard

### Cell 8 — Forecasting Model
- Features: lag variables, cyclical encoding, day-of-week, weekend flags
- Models compared: Linear Regression vs Random Forest
- Best model selected based on MAE, RMSE, R² comparison

### Cell 9 — 30-Day Forecast
- Random Forest forecast for next 30 days
- Peak day: 396,000 updates | Lowest: 207,000 updates
- Interactive forecast visualization with historical context

### Cell 10 — Anomaly Detection System
- Z-score based global anomaly detection (threshold: 2.5σ)
- Local anomaly detection using 7-day rolling deviation
- Visual flagging of anomaly days on time series chart

### Cell 11 — District & Pincode Hotspot Analysis
- Top 15 district hotspots by total update volume
- Top 15 pincode hotspots with daily average intensity
- High-intensity pincode identification (top 5% by daily volume)

### Cell 12 — State Clustering (K-Means)
- K-Means clustering of states into 4 segments
- Clusters: High Volume Leaders, Youth Dominated, Moderate, Low Volume
- Interactive scatter plot: Updates vs Youth Ratio by cluster

### Cell 13 — Resource Optimization Model
- Resource score formula: 50% volume + 25% intensity + 15% geography + 10% complexity
- Recommended allocation of 10,000 staff across all states
- Required update centres per state based on peak capacity model
- Output: Exported CSV — UIDAI_Resource_Allocation_Plan.csv

### Cell 14 — Executive Dashboard
- 9-panel interactive Plotly dashboard
- Indicators, pie charts, bar charts, time series, forecast summary
- Built for UIDAI leadership decision-making

### Cell 15 — Final Recommendations
- 4 strategic recommendations with projected impact
- 5 innovative proposals: Predictive Demand App, AI Rostering, Live Dashboard, Feedback Loop, Hyper-Local Outreach

---

## Tech Stack

![Python](https://img.shields.io/badge/Python-3.11-blue)
![Pandas](https://img.shields.io/badge/Pandas-2.2-green)
![Scikit--learn](https://img.shields.io/badge/Scikit--learn-1.8-orange)
![Plotly](https://img.shields.io/badge/Plotly-5.x-purple)

`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `Plotly` · 
`Scikit-learn` · `KMeans` · `Random Forest` · `Linear Regression`

---

## Key Business Insights

**1. Geographic Concentration**
Top 5 states (UP, Maharashtra, Bihar, West Bengal, MP) generate 68.7% of 
all demographic updates — resource allocation must reflect this imbalance.

**2. Adult-Driven Demand**
90.1% of updates come from adults (18+), primarily driven by address changes 
and mobile number updates linked to migration and employment.

**3. Saturday Surge**
Saturday averages 1,115,578 updates — 3x the Sunday average of 316,086. 
Weekend staffing strategy must be completely restructured.

**4. Forecast Accuracy**
30-day forecast projects 10.32 million updates with daily peaks on Saturdays. 
Proactive staffing based on this model could reduce wait times by 45%.

---

## Strategic Recommendations

| # | Recommendation | Expected Impact |
|---|---------------|----------------|
| 1 | Allocate 60–70% capacity to top 5 states | Immediate queue reduction |
| 2 | Reduce Sunday ops, boost Tuesday–Wednesday | 30% better staff utilization |
| 3 | Launch School Aadhaar Drive in youth-heavy districts | 15% youth update compliance |
| 4 | Deploy real-time anomaly alert system | Proactive crisis management |

---

## How to Run

1. Open `UIDAI_Demographic_Updates.ipynb` in Google Colab
2. Upload the 5 Aadhaar CSV dataset files when prompted
3. Click **Runtime → Run all**

> Dataset available via UIDAI Hackathon portal.

---

## Author

**Gundavaram Likhitha Rao**  
B.Tech CSE-AIML | SR University, Telangana  
[GitHub](https://github.com/Likhitha-26-AI)
