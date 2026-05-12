# 💊 Pharmaceutical Sales Analytics Dashboard

> End-to-end data analysis project covering sales performance across Germany and Poland (2017–2020) — from raw data cleaning in Python to an interactive Power BI dashboard.

---

## 📌 Project Overview

This project analyzes **251,418 pharmaceutical sales transactions** from two markets — Germany and Poland — spanning four years (2017–2020). The goal is to surface actionable insights on sales performance by product category, distribution channel, sales team, and geography, delivered through a fully interactive Power BI dashboard.

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Python** (pandas) | Data cleaning, deduplication, EDA |
| **Jupyter Notebook** | Exploratory analysis workflow |
| **Power BI** | Interactive dashboard & visualization |
| **CSV / Excel** | Raw and cleaned data storage |

---

## 📊 Dataset

| Attribute | Detail |
|-----------|--------|
| Cleaned rows | **251,418** |
| Columns | 19 |
| Time period | 2017 – 2020 |
| Markets | 🇩🇪 Germany, 🇵🇱 Poland |
| Cities covered | 749 |

**Key columns:**
- `Distributor`, `Customer Name`, `City`, `Country`, `Latitude`, `Longitude`
- `Channel` (Hospital / Pharmacy), `Sub-channel` (Government, Institution, Private, Retail)
- `Product Name` (240 unique), `Product Class` (6 categories)
- `Quantity`, `Price`, `Sales`
- `Month`, `Year`
- `Name of Sales Rep` (13 reps), `Manager` (4 managers), `Sales Team` (Alfa, Bravo, Charlie, Delta)

---

## 🔧 Data Cleaning Steps

Performed in `data_exploration.ipynb` using pandas:

1. Loaded raw data — inspected shape, dtypes, and summary statistics
2. Checked for nulls — `df.isnull().sum()`
3. Removed duplicates — `df.drop_duplicates()`
4. Filtered invalid records — removed rows where `Quantity < 0`
5. Verified team–manager mapping — confirmed 1 unique manager per sales team
6. Exported cleaned file — `df_cleaned.csv`

---

## 📈 Key Findings

### Revenue Overview
| Year | Revenue |
|------|---------|
| 2017 | $2.72B |
| 2018 | $3.55B *(peak)* |
| 2019 | $2.96B |
| 2020 | $2.72B |

**Total (2017–2020): ~$11.9 Billion**

### By Product Category
| Product Class | Total Sales | Share |
|---------------|-------------|-------|
| Analgesics | $2,403M | 20.1% |
| Antiseptics | $2,263M | 18.9% |
| Mood Stabilizers | $2,079M | 17.4% |
| Antipiretics | $1,911M | 16.0% |
| Antibiotics | $1,776M | 14.9% |
| Antimalarial | $1,513M | 12.7% |

---

## 📉 Dashboard Highlights (Power BI)

The `dashboard.pbix` file contains an interactive report with:
- Sales trend over time (monthly & yearly)
- Revenue breakdown by Product Class
- Hospital vs Pharmacy channel performance
- Sales team & rep leaderboard
- Slicers — Year, Country, City

> Open `dashboard.pbix` with [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)

---

## 🚀 How to Run

**Python (Data Cleaning)**
```bash
pip install pandas jupyter
jupyter notebook data_exploration.ipynb
```

**Power BI Dashboard**
1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/)
2. Open `dashboard.pbix`

---

## 💡 Recommendations

1. **Investigate the 2018 spike** — Revenue jumped 30% vs 2017. Identifying the driver (product, region, campaign) could inform future growth strategy.
2. **Channel profitability** — Hospital vs Pharmacy volume is clear; analyzing margin per channel would sharpen resource allocation.
3. **Rep-level performance** — 13 reps across 4 teams; quota attainment analysis would surface coaching opportunities.

---

## 👤 Author

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin)](www.linkedin.com/in/ade-eriyanto)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?style=flat&logo=github)](https://github.com/adeeriyanto)
