# Covid19-global-analysis
End-to-end global COVID-19 analytics project with data cleaning, feature engineering, EDA, hotspot maps, and ARIMA forecasting using OWID dataset.
# 🌍 COVID-19 Global Analysis — End-to-End (EDA + Forecasting)

An end-to-end analytics project on global COVID-19 data using the **Our World in Data (OWID)** dataset.  
You’ll load data, clean it, engineer key public-health metrics (CFR, positivity, moving averages), do EDA (trends, country comparisons, hotspot map), and build a **30-day ARIMA forecast**.

> **Why this repo?**  
> Shows full data-analysis workflow: data access → cleaning → feature engineering → visuals → forecasting — all reproducible in **Jupyter Notebook**.

---

## 📊 Key Features

- Clean, reproducible notebook (Jupyter)
- Public-health metrics:
  - **CFR** = total_deaths / total_cases  
  - **Positivity (est.)** = new_cases / new_tests  
  - **7-day moving averages** for stable trends
- Visuals:
  - Global trend line (7-day MA)
  - Country comparison charts
  - World hotspot choropleth (latest day)
- **Forecasting**: ARIMA 30-day global forecast
- Outputs saved to `data/processed/` (small files suitable for BI tools)

---


> ⚠️ **Note:** The OWID CSV is ~100MB; it’s **not included** in the repo to avoid GitHub size limits.  
> The notebook downloads it automatically.

---

## 🧰 Tech Stack

- **Python**: pandas, numpy, plotly, statsmodels
- **Notebook**: Jupyter / VS Code
- (Optional) **Prophet** for alternative forecasting

---

## 🗃️ Dataset

- **Source:** Our World in Data (OWID)  
- **Direct CSV (recommended in code):**  
  https://github.com/owid/covid-19-data/raw/master/public/data/owid-covid-data.csv

Columns include per-country daily metrics for cases, deaths, tests, vaccinations, population, etc.

---

## 🚀 How to Run (Jupyter — no terminal required)

1. Open `notebooks/covid_analysis.ipynb`.
2. Run cells **top → bottom**.

### 1) Create folders (first cell)
```python
import os
os.makedirs("data/raw", exist_ok=True)
os.makedirs("data/processed", exist_ok=True)
print("folders ready ✅")


## 🗂️ Repository Structure

