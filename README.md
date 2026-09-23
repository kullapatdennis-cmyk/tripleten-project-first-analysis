# NYC Parks Inspection KPI Report

**View the full workbook:** [NYC Parks Inspection KPI Report (Google Sheets)](https://docs.google.com/spreadsheets/d/1_CJdD44ce8q1yMrgrTTpIT0E2f0bKbdYYsIEl7Nlxdg/edit?usp=sharing)

## Project Overview

This project analyzes NYC Parks inspection records from 2020 to 2025 to measure how clean the city's parks are and to identify where and when cleanliness falls short. The analysis breaks results down by borough, district, season, and year to surface trends and problem areas.

**Business question:** Are NYC parks meeting the Parks Department's mission of keeping parks clean and cared for, and where should resources be focused to improve?

## Dataset

- **Source:** [NYC Parks Inspection Program dataset](https://data.cityofnewyork.us/dataset/Parks-Inspection-Program-Inspections/yg3y-7juh/about_data)
- **Size:** 36,481 inspection records after cleaning
- **Period:** 2020–2025
- **Key fields:** borough, district, season, inspection date, inspector, overall condition, and cleanliness rating (Acceptable / Unacceptable / Not Rated)

## Tools & Techniques

- **Google Sheets**
- **Data cleaning:** `SUBSTITUTE()`, `TRIM()`, removing blanks, checking for duplicates with `IF()` + `COUNTIF()`
- **Data integrity:** data validation rules and conditional formatting for rating columns
- **Analysis:** calculated helper columns with nested `IF()` formulas and pivot tables
- **Reporting:** KPI dashboard with a North Star metric plus leading and lagging indicators

## Process

1. **Cleaned the raw data.** I standardized number and date formats, removed incomplete records, and checked for duplicates. Every change is documented in the `data_cleaning_log` sheet, including what was changed, why, and how many rows were affected.
2. **Defined the KPI.** I chose **Cleanliness Rate** (the percentage of inspections rated Acceptable) as the North Star metric, because it directly measures the Parks Department's mission of keeping parks clean.
3. **Built pivot tables** to compare cleanliness across boroughs, districts, seasons, and years.
4. **Created a dashboard** that pairs the North Star KPI with leading indicators (inspection volume) and lagging indicators (Cleanliness Rate and year-over-year trend).
5. **Wrote observations and recommendations** based on the findings.

## Key Findings

- **Overall health is good:** The Cleanliness Rate is **92.5%** across all inspections.
- **Performance is stable:** The rate stayed above 90% every year from 2020 to 2025, with only small year-over-year changes.
- **Seasonal pattern:** Parks perform best in **Spring (~94%)** and worst in **Summer (~90.4%)**.
- **Problem area:** **District 18** has the lowest Cleanliness Rate at **84.96%**, about 7.5 percentage points below average.
- **Borough gap:** **Brooklyn** consistently has the lowest Cleanliness Rate of all boroughs.

## Recommendations

- **Summer:** Investigate the summer dip, since it may reflect heavier park use, and consider adding cleaning capacity during peak months.
- **District 18 and Brooklyn:** Look into the root causes of lower performance, such as staffing, visitor volume, or inspection timing, and target support there.

## Workbook Structure

| Sheet | Description |
|---|---|
| README | Project summary and sheet guide |
| raw_data | Original, unchanged inspection records |
| cleaned_data | Cleaned and standardized data with calculated columns |
| data_cleaning_log | Step-by-step record of every cleaning decision |
| Pivot Tables | Summaries by borough, district, season, and year |
| Dashboards | North Star KPI with leading and lagging indicators |
| Observations & Recommendations | Findings and suggested actions |

## Author

**Kullapat Dennis**
[LinkedIn](https://www.linkedin.com/in/kullapat-dennis-a5435717b/)
