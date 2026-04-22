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

![Executive Summary](01-Executive%20Summary.png)

Eight KPI tiles covering total gross profit, total revenue, and total cost each shown against planned figures, plus gross profit margin %, revenue variance %, cost variance %, new customers, and lost customers. Gross profit by region and product line. Revenue by RAG Status showing revenue distribution across Green, Amber, and Red performing records.

RAG Status thresholds based on revenue variance vs planned:
- Green: greater than 3%
- Amber: between -3% and 3%
- Red: below -3%

---

**Page 2: Revenue Performance Analysis**

![Revenue Performance Analysis](02-Revenue%20Performance.png)

Revenue variance heatmap by region and product line showing variance percentages color coded from red for underperformance to green for outperformance. Revenue variance by region and product line in USD. Revenue vs Gross Margin by Region scatter plot with Revenue Actual on the X axis, Gross Margin % on the Y axis, bubble size representing Headcount, and Region as color.

---

**Page 3: Cost Performance Analysis**

![Cost Performance Analysis](03-Cost%20Performance.png)

Cost variance heatmap by region and product line. Cost variance by region and product line with diverging bar charts where negative values represent underspend which is favorable and positive values represent overspend which is unfavorable, reflecting standard financial reporting convention. Actual vs Planned Cost by Region clustered bar chart showing Cost Actual vs Cost Planned side by side for all five regions.

---

**Page 4: Profitability Performance Analysis**

![Profitability Performance Analysis](04-Profitability%20Performance.png)

Gross profit margin % heatmap across all region and product line combinations, all cells green reflecting healthy margins across the board. Gross profit by region and product line. Gross Profit vs Gross Margin by Region scatter plot with Gross Profit Actual on the X axis, Gross Margin % on the Y axis, bubble size representing Headcount, and Region as color.

---

**Page 5: Year Over Year Trends**

![Year Over Year Trends](05-Year%20over%20Year%20Trends.png)

Monthly Revenue vs Cost Trend 2023-2024 showing the profitability gap visually across 24 months. Monthly Cost Performance Actual vs Planned. Quarterly Gross Profit Performance 2023 vs 2024 grouped bar chart. Net Customer Movement by Month showing new customers vs lost customers across both years.

---

## Key Business Insights

- Total revenue of $165.3M exceeded planned by 0.81% with costs controlled at only 0.10% over planned
- Cloud Solutions leads gross profit at $31.0M with a consistent 47-48% gross margin across all five regions
- North America drives the highest gross profit at $23.6M
- Latin America consistently underperforms on revenue volume but shows favorable cost control, its challenge is scale not efficiency
- Hardware carries the lowest gross margin at 27-29% across all regions reflecting physical product cost structures
- Gross margins remained stable between 39% and 44% across both years indicating consistent cost management
- New customer acquisition of 3,957 outpaced customer loss of 1,272 in every single month across both years
- Every quarter in 2024 outperformed the equivalent quarter in 2023

---

## Technical Challenges

**Heatmap color scale with negative values:**
SAC's gradient palette rejects negative numbers in the color scale settings. Solved by creating CM_Variance_Index dividing Revenue Actual by Revenue Budget, producing positive values above and below 1.0. The midpoint position was then shifted to 70% through iterative experimentation to correctly map the color logic given SAC's relative rather than absolute scaling behavior.

**Month ordering in charts:**
SAC defaulted to sorting Month Label alphabetically, producing a nonsensical timeline. Solved by replacing Month Label with the numeric Month dimension which SAC sorts correctly from 1 through 12. The axis label was then renamed to Month for readability.

**Dual axis chart with incompatible scales:**
Layering revenue in millions and margin percentages on one chart produced a confusing visual. Solved by splitting into two focused charts, one showing the Revenue vs Cost trend and one showing Monthly Cost Actual vs Planned.

**Y axis minimum override:**
SAC does not expose a minimum value setting for line chart axes in the styling panel. The gross margin trend chart defaults to starting at 0% despite all data sitting between 39% and 44%. Accepted as a known platform limitation. A workaround noted for future builds is to pre-calculate a scaled measure that compresses the range before import.

**Headcount aggregation error on scatter plot:**
When building the cost scatter plot, the chart displayed values of 19, 25, 9, 11, and 33 instead of the expected millions-level cost figures. The chart was counting records rather than summing cost values due to residual configuration settings carried over from a previous bubble chart that used Headcount as its size measure. Solved by deleting the chart entirely and rebuilding from scratch with clean configuration, which correctly aggregated Cost Actual and Cost Planned as SUM measures.

**Table chart configuration:**
SAC's table chart type requires dimensions in rows and measures in columns using a specific drag and drop workflow that is not immediately intuitive. Initial attempts produced a single cell table. Solved by replacing the table with a grouped bar chart showing Quarterly Gross Profit Performance by year, which delivered the same story in a more visually impactful format.

---

## Tools and Techniques

**Platform:** SAP Analytics Cloud, Story Builder, Canvas layout

**Data:** Python generated CSV, 480 rows, 27 columns

**Modeler:** Custom dimensions, semantic types, calculated measures including variance percentage, gross margin, net customer movement, and variance index

**Skills:** Actuals vs planned analysis, gross margin analysis, cost variance monitoring, RAG framework, regional benchmarking, YoY trend analysis, executive dashboard design, cost efficiency analysis

---

## Author

**Bate Bita Tambe**
Financial and Business Intelligence Analyst
[LinkedIn](https://www.linkedin.com/in/bate-bita-tambe) | [GitHub](https://github.com/bate-bita)
```
