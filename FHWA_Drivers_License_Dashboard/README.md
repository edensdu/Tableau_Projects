# 📊 Driver’s License Distribution by Age and Gender (1963–2023)

**Dashboard built in Tableau Public**  
**Date Published:** April 6, 2025  
**Data Source:** FHWA Highway Statistics Table DL-220  
### 🔗 View Dashboard on Tableau Public  
[Click here to explore the interactive dashboard](https://public.tableau.com/app/profile/edens.duphresne5020/viz/License_Dashboard/License_Dashboard?publish=yes)


---

## 🧠 Overview

This Tableau dashboard provides a comprehensive look at the distribution of U.S. driver’s licenses from **1963 to 2023**, segmented by **age cohort** and **gender**. Using historical data from the Federal Highway Administration (FHWA), this project highlights demographic trends in driver licensing and showcases gender parity progression over time.

The dashboard is designed for ease of exploration with filters, KPIs, stacked bars, and a dual-line time series — making it suitable for analysts, transportation policymakers, and data science employers interested in visualization capabilities.

---

## 📊 Key Features

### ✅ **Top-Level Metrics (KPIs)**
- **Total Licensed Drivers** from 1963 to 2023
- **% Male** and **% Female** calculated using custom formulas
- Dynamic updates based on user filters for **Cohort** and **Year**

### 📊 **Drivers by Age Cohort and Sex**
- Stacked horizontal bar chart showing the breakdown of male and female drivers by age group
- Highlights which age brackets have the highest licensing numbers
- Shows how gender distribution varies across different age cohorts

### 📈 **Sex Distribution Over Time**
- Dual-line time series comparing the total number of male and female licensed drivers annually
- Highlights the trend of increasing female license holders and how the gender gap has narrowed over time

### 🎛️ **Interactive Filters**
- Filter by `Year` and `Cohort` to drill into specific demographics or points in time

---

## ⚙️ Technical Details & Tableau Calculations

### 📂 Dataset Source:
- **FHWA Highway Statistics Table DL-220**
- Aggregated by Year, Age Cohort, and Sex
- Cleaned and structured directly in Tableau (no outside preprocessing)

## 📐 Tableau Calculated Fields

These calculated fields were created in Tableau to drive the KPIs and gender-based breakdowns in the dashboard.

```tableau
// Number of Male Drivers
IF [Sex] = "Male" THEN [Drivers] END

// Number of Female Drivers
IF [Sex] = "Female" THEN [Drivers] END

// % Male
SUM([Number_of_Males]) / SUM([Drivers])

// % Female
SUM([Number_of_Females]) / SUM([Drivers])
