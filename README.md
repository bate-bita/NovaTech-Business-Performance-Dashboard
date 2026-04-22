# NovaTech Business Performance Dashboard | SAP Analytics Cloud

A five page executive BI dashboard built from scratch in SAP Analytics Cloud, analyzing 24 months of fictional business performance data for NovaTech Solutions, a global technology company operating across 5 regions, 4 product lines, and 11 countries.


---

## Project Overview

**Goal:** Build a multi page interactive executive dashboard that tells a complete business performance story from high level summary through revenue, cost, profitability, and year over year trend analysis.

**Tool:** SAP Analytics Cloud (SAC), an enterprise BI platform used by major corporations worldwide.

**Dataset:** 480 rows of fictional business data generated in Python, covering January 2023 to December 2024.

---

## Dashboard Pages

**Page 1: Executive Summary**
Eight KPI tiles covering revenue, profit, cost, margins, variances, and customer movement. Profit by region and product line. RAG performance status distribution.

**Page 2: Revenue Performance Analysis**
Revenue variance heatmap by region and product line. Revenue variance by region and product line. Revenue vs profitability scatter plot.

**Page 3: Cost Performance Analysis**
Cost variance heatmap by region and product line. Cost variance by region and product line with green and red coloring reflecting standard financial reporting convention where cost underspend is favorable. Cost vs profitability scatter plot.

**Page 4: Profitability Performance Analysis**
Gross profit margin heatmap across all region and product line combinations. Gross profit by region and product line. Gross margin vs profitability by country scatter plot.

**Page 5: Year over Year Trends**
Revenue vs cost trend showing the profitability gap visually across 24 months. Monthly cost performance actual vs budget. Quarterly gross profit performance 2023 vs 2024. New vs lost customer movement by month.

---

## Key Business Insights

- Total revenue of $165.3M exceeded budget by 0.81% with costs controlled at only 0.10% over budget
- Cloud Solutions leads revenue at $64.5M with a 48% gross margin
- North America drives the highest profit at $23.6M
- Latin America consistently underperforms on revenue but shows favorable cost control
- Gross margins remained stable between 39% and 44% across both years
- New customer acquisition outpaced attrition in every single month across both years

---

## Technical Challenges

**Heatmap color scale with negative values:**
SAC's gradient palette rejects negative numbers. Solved by creating CM_Variance_Index dividing actual by budget, producing positive values above and below 1.0. The midpoint position was then shifted to 70% through iterative experimentation to correctly map the color logic given SAC's relative rather than absolute scaling behavior.

**Month ordering in charts:**
SAC defaulted to sorting Month Label alphabetically. Solved this by manually reordering the Month dimension, to fit the proper calendar chronology.

**Dual axis chart with incompatible scales**
Layering revenue in millions and margin percentages on one chart produced a confusing visual. Solved this by splitting into two focused charts.

**Y axis minimum override**
SAC does not expose a minimum value setting for line chart axes in the styling panel. Accepted as a known platform limitation.

---

## Tools and Techniques

**Platform:** SAP Analytics Cloud, Story Builder, Canvas layout

**Data:** Python generated CSV, 480 rows, 27 columns

**Modeler:** Custom dimensions, semantic types, calculated measures including variance percentage, gross margin, net customer movement, and variance index

**Skills:** Actuals vs budget analysis, gross margin analysis, cost variance monitoring, RAG framework, regional benchmarking, YoY trend analysis, executive dashboard design

---

## Author

**Bate Bita Tambe**

Financial and Business Intelligence Analyst

[LinkedIn](https://www.linkedin.com/in/bate-bita-tambe)
