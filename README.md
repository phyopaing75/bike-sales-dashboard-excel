Project Overview
This project analyzes demographic, socioeconomic, and commuting characteristics influencing customer bike purchasing decisions. Using raw customer transaction and survey data, the dataset was cleaned, categorized, and modeled in Microsoft Excel to uncover key purchase drivers and present executive-ready insights via an interactive dashboard.

---

Dataset & Structure
The workbook contains four dedicated sheets reflecting an end-to-end analytical workflow:
  1. bike_buyers (Raw Data): Original dataset containing 1,000 customer records and 13 attributes including customer ID, marital status, gender, income, education, occupation, home ownership, number of cars, commute distance, region, and age.
  2. work_sheet (Data Cleaning & Feature Engineering): Transformed dataset with standardized labels, removed duplicates, and engineered categorical fields.
  3. pivot_table (Data Modeling & Aggregation): Aggregated metrics exploring customer segments across demographic and commute dimensions.
  4. dashboard (Visualization & Reporting): Interactive visual dashboard equipped with slicers for dynamic filtering.

---

Data Cleaning & Transformation
* Deduplication: Identified and removed duplicate customer entries to maintain integrity.
* Value Standardization:
1. Standardized abbreviated marital status codes (M -> Married, S -> Single).
2. Standardized gender values (M -> Male, F -> Female).
3. Feature Engineering (Age Bucketing): Grouped continuous customer age into distinct life stages using nested logical conditions:
4. Adolescent: Under 31 years old
5. Middle Age: 31 to 54 years old
6. Old: 55 years and older

---

Key Insights & Findings
1. Income Level: Customers who purchased a bike earned a higher average income (~$58,000) compared to non-buyers (~$54,900) across both male and female demographics.
2. Commute Distance: Bike purchases peaked heavily among individuals with a commute distance of 0–1 miles (200 buyers), with purchase likelihood steadily decreasing as commute distances exceeded 5 miles.
3. Age Demographics: The Middle Age (31–54) demographic represented the largest customer base and the highest purchase volume (383 buyers), significantly outpacing adolescents and older age brackets.

---

Interactive Dashboard Features
1. Average Income by Gender & Purchase Status: Clustered bar/column comparison highlighting purchasing power.
2. Customer Commute Distribution: Line/bar trend tracking bike adoption across commute brackets.
3. Bike Purchases by Age Group: Segmented breakdown across life stages.
4. Dynamic Slicers: Interactive filtering by Marital Status, Education Level, and Region to allow targeted exploratory data analysis.

---

Tools & Skills Demonstrated
1. Tool: Microsoft Excel
2. Techniques: Data Cleaning, Formula Modeling (IF / nested conditions), Pivot Tables, Pivot Charts, Slicers & Report Connections, Dashboard Design & Layout.
