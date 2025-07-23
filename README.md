# 💼 IT Services General BI Dashboard

This project is a comprehensive **Business Intelligence solution** designed using **Power BI** and **SQL** to monitor key performance indicators (KPIs), project progress, resource utilization, and bug tracking across IT service operations.

---

## 📊 Dashboard Overview

The interactive Power BI dashboard includes the following key features:

- **Total Hours Billed**: Visual representation of total hours logged (52M).
- **Average Resource Utilization**: Displays average efficiency of resources (70.03%).
- **Bugs vs Hours Comparison**: Bar chart showing correlation between bugs and time spent.
- **Bugs vs Utilization**: Pie chart comparing bug count and resource utilization.
- **Project-Wise Bug Reports**: Tabular data showing total bugs reported by project.
- **Project Completion Days**: Table showing duration of each project.
- **Year & Quarter Filters**: Allows filtering data by year (2022–2024) and quarters (Q1–Q4).
- **Pie Chart Analysis**: Breakdown of bugs resolution availability (Yes/No/Not Available).

---

## 🧠 Key Insights & Features

- Quickly identify **high-bug projects** and **underutilized resources**.
- Monitor **SLA compliance**, project delays, and overall delivery timelines.
- Helps in **project planning** and **resource optimization**.
- Supports filtering by **year** and **quarter** for focused analysis.

---

## 🗃️ Technologies Used

- **SQL Server**: Data cleansing, transformation, and aggregation.
- **Power BI**: Interactive dashboard creation and data visualization.
- **DAX**: For KPIs, conditional formatting, and calculated measures.

---

## 🧾 SQL Scripts & Logic

Here are some examples of the SQL logic used in backend:

```sql
-- Replace NULL values with average
UPDATE IT
SET Hours_Billed = '1045'
WHERE Hours_Billed IS NULL;

-- Average Resource Utilization
SELECT AVG(Resource_Utilization) AS AVG_RESOURCE FROM IT;

-- Total Hours Billed
SELECT SUM(Hours_Billed) AS TOTAL_HOURS FROM IT;

-- Bugs Reported per Project
SELECT PROJECT_ID, SUM(Bugs_Reported) AS Reported_Bugs
FROM IT
GROUP BY PROJECT_ID;


