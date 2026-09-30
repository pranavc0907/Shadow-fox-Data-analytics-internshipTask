# Beginner Level — Sample Superstore Sales & Profit Dashboard

**ShadowFox Data Analyst Internship — Level 1 (Beginner)**

## Overview
This project analyzes the Sample Superstore dataset — a retail dataset covering
Furniture, Office Supplies, and Technology orders across the US — and presents
the findings as a spreadsheet-based dashboard with key metrics, category/region/
segment breakdowns, and business-oriented insights.

## Dataset
- **Source:** Sample Superstore dataset (Kaggle)
- **File:** `SampleSuperstore.csv`
- **Size:** 9,994 rows, 13 columns
- **Fields:** Ship Mode, Segment, Country, City, State, Postal Code, Region,
  Category, Sub-Category, Sales, Quantity, Discount, Profit
- **Note:** this version of the dataset has no Order Date column, so trend
  analysis is done by Category / Sub-Category / Region / Segment rather than
  by month.

## Data Cleaning
- Removed 17 exact duplicate rows (9,994 → 9,977 rows)
- Verified no missing values across any column
- Converted the cleaned range into an Excel Table for reliable formula ranges

## Approach
All analysis is built with live formulas (`SUMIFS`, `COUNTIFS`, `SUM`,
`AVERAGE`) referencing a single `Raw Data` tab, so every KPI, table, and chart
recalculates automatically if the source data changes. No values are
hardcoded.

**Workbook structure:**
| Tab | Contents |
|---|---|
| Raw Data | Cleaned dataset as an Excel Table |
| Summary Dashboard | KPI cards: Total Sales, Total Profit, Orders, Margin, AOV, Avg Discount |
| Category Analysis | Sales/Profit/Margin by Category, with chart |
| Sub-Category Analysis | All 17 sub-categories ranked by profit, with chart |
| Region Analysis | Sales/Profit/Margin by Region, with chart |
| Segment Analysis | Sales/Profit/Margin by Customer Segment, with chart |
| Discount Impact | Profit margin by discount band, with chart |
| Insights & Recommendations | Written findings tied to each analysis tab |

## Key Metrics
- Total Sales: **$2,296,196**
- Total Profit: **$286,241**
- Overall Profit Margin: **12.5%**
- Total Orders: **9,977**
- Avg Order Value: **$230.15**
- Avg Discount Given: **15.6%**

## Key Findings
- **Technology (17.4%) and Office Supplies (17.0%)** margins are healthy;
  **Furniture (2.5%)** is barely profitable despite comparable revenue.
- **Tables** are the single worst-performing sub-category: -8.6% margin,
  -$17.7K in losses — the main drag on the whole Furniture category.
- **West region** leads on profitability (14.9% margin); **Central** lags
  (7.9% margin) despite similar order volume.
- **Home Office** is the smallest segment by revenue but the most profitable
  per dollar of sales (14.0% margin); **Consumer** is the largest segment but
  the least profitable (11.5%).
- **Discounting above ~20% turns orders unprofitable.** Margin is 29.5% at
  0% discount, falls to -10.1% at 20-30% discount, and -119.2% at 50%+
  discount — the clearest and most actionable pattern in the dataset.

## Recommendations
1. Tighten discounting policy above the 20% threshold — orders past that
   point are reliably unprofitable across the dataset.
2. Investigate the Tables sub-category specifically (cost, pricing, or
   discount practices).
3. Study what drives the West region's and Home Office segment's stronger
   margins and look for ways to apply that elsewhere (Central, Consumer).
4. Continue prioritizing Technology and Office Supplies, which combine
   strong revenue with healthy margins.

## Tools Used
Excel (formulas: `SUMIFS`, `COUNTIFS`, `SUM`, `AVERAGE`; native bar/line charts)

## Files
- `Superstore_Beginner_Dashboard.xlsx` — the full dashboard workbook
- `SampleSuperstore.csv` — original raw dataset
