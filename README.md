# Bike Sales Analysis: Excel Customer Segmentation Dashboard

[![Excel](https://img.shields.io/badge/Microsoft_Excel-Pivot_Dashboard-217346?style=flat&logo=microsoftexcel&logoColor=white)](https://www.microsoft.com/microsoft-365/excel)

---

## Project Overview

* Tools and Technologies: Microsoft Excel (nested `IF` formulas, PivotTables, PivotCharts, Slicers)
* Dataset Scope: 1,026 raw customer records, reduced to 1,000 after removing 26 duplicates. Each record has 13 attributes: marital status, gender, income, children, education, occupation, home ownership, cars, commute distance, region, age and whether the customer purchased a bike.
* Workbook: `bike-sales.xlsx`

---

## Business Problem

A bike retailer wants to know which kinds of customers are most likely to buy a bike, so marketing can focus on them instead of treating every customer the same. The raw survey data holds abbreviated codes and a continuous age field, and it contains duplicate records. This project cleans the data in Excel and builds an interactive dashboard that compares buyers and non-buyers by income, commute distance and age.

---

## Business Questions

| # | Business question | Dashboard view |
|---|---|---|
| 1 | Do bike buyers earn more than non-buyers, for both men and women? | Average Income by Gender and Purchase Status |
| 2 | How does commute distance relate to buying a bike? | Customer Commute Distribution |
| 3 | Which age group buys the most bikes? | Bike Purchases by Age Group |
| 4 | Do these patterns change by marital status, education or region? | Slicers: Marital Status, Education, Region |

---

## Key Insights

Insights 1 to 4 come straight from the three pivot tables on the `pivot_table` sheet. Insights 5 and 6 come from the same pivots after selecting a value in the Marital Status, Region or Education slicer. Purchase rates are buyers divided by all customers in the group.

1. **Buyers earn more on average.** The average income is $57,963 for buyers and $54,875 for non-buyers.
2. **The income gap holds for both genders.** Male buyers average $60,124 against $56,208 for male non-buyers, and female buyers average $55,774 against $53,440 for female non-buyers. Men earn more than women in both groups.
3. **Short commutes have the most buyers, but the highest purchase rate is at 2 to 5 miles.** The 0 to 1 mile group has the most buyers (200 of 366, 54.6%), and 2 to 5 miles has the highest rate (95 of 162, 58.6%). Purchase rates are lower for longer commutes: 39.6% at 5 to 10 miles and 29.7% above 10 miles.
4. **Middle-aged customers (31 to 54) are the largest buying group, and they buy at the highest rate.** They account for 383 of the 481 buyers, with a purchase rate of 54.6%, against 35.5% for adolescents (under 31) and 31.2% for older customers (55 and over).
5. **Single customers buy more than married customers.** Selecting each value in the Marital Status slicer shows a purchase rate of 54.1% for single customers (250 of 462) and 42.9% for married customers (231 of 538).
6. **Region and education also change the rate.** With the Region slicer, the Pacific region has the highest rate (58.9%, 113 of 192), against 49.3% in Europe (148 of 300) and 43.3% in North America (220 of 508). With the Education slicer, customers with a Bachelors degree (55.2%) or a Graduate Degree (54.0%) buy more than those with only partial high school (26.3%).
7. **Overall, 48.1% of customers bought a bike** (481 of 1,000), so the segments above can be compared against that baseline.

---

## Recommendations

1. **Target middle-aged customers (31 to 54) in marketing.** They are 70% of customers and 80% of buyers, and they buy at a higher rate than the other age groups.
2. **Focus on customers with a commute under 5 miles.** Together they buy at a rate of 53.4% (372 of 697), against 36.0% (109 of 303) for customers who commute 5 miles or more.
3. **Prioritise single customers and the Pacific region for campaigns.** Both buy at a higher rate than the 48.1% average, while North America (43.3%) and married customers (42.9%) buy at a lower rate and may need a different offer.

---

## Data Cleaning and Transformation

* Deduplication: 26 duplicate records removed (1,026 to 1,000 rows).
* Marital status standardized: `M` to Married, `S` to Single.
* Gender standardized: `M` to Male, `F` to Female.
* Age brackets created in `work_sheet` with a nested `IF`: Adolescent (under 31), Middle Age (31 to 54), Old (55 and over).

---

## Dashboard Design

| Sheet | Content |
|---|---|
| `bike_buyers` | Raw data (1,026 rows) |
| `work_sheet` | Cleaned data with the age bracket field (1,000 rows) |
| `pivot_table` | Three pivot tables: average income by gender and purchase, purchases by commute distance, purchases by age bracket |
| `dashboard` | Three pivot charts with slicers for Marital Status, Education and Region |

---

## Data Notes

* **This is survey data, so the findings show association, not cause.** A group buying more does not mean the group trait made them buy.
* **The pivot tables show counts, not rates.** Purchase rates in the insights are calculated from those counts. Add a rate field to the pivot if you want them on the dashboard.
* **Income alone is a weak guide.** The average gap between buyers and non-buyers is about $3,100, so test income together with age and commute distance.
* **Segment sizes differ.** Some groups are small, such as partial high school (76 customers), so their rates are less reliable.
* **Age brackets are broad.** Customers aged 31 to 54 form one group, so differences within it are hidden.

---

## How to Open

1. Open `bike-sales.xlsx` in Microsoft Excel.
2. Go to the `dashboard` sheet and use the slicers to filter all charts together.

---

## Repository Contents

| File | Description |
|---|---|
| `bike-sales.xlsx` | Workbook with raw data, cleaned data, pivot tables and the dashboard |
| `README.md` | Project documentation |
