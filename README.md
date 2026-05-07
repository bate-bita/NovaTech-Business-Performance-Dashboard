# NovaTech Business Performance Dashboard | SAP Analytics Cloud

A five-page interactive executive business intelligence dashboard built from scratch in SAP Analytics Cloud (SAC), analyzing 24 months of fictional business performance data for a global technology company called NovaTech Solutions. The dashboard covers revenue, cost, gross profit, and customer movement across 5 regions, 4 product lines, and 11 countries from January 2023 to December 2024.

---

## Project Overview

**Business Context:** NovaTech Solutions is a fictional global technology company operating across North America, Europe, Asia Pacific, Middle East and Africa, and Latin America. The dashboard was designed to mirror the kind of executive reporting tool a Financial or Business Intelligence Analyst would build and maintain in a real corporate environment.

**Goal:** Build a five-page interactive executive dashboard that tells a coherent business performance story from high-level summary to regional drill-down to year-over-year trend analysis.

**Tool:** SAP Analytics Cloud (SAC), an enterprise business intelligence platform used by major corporations worldwide.

**Dataset:** 480 rows of fictional business data generated in Python, covering 24 months across 5 regions, 4 product lines, and 12 product categories. All data is fictional and was purpose-built for this project. 

Preview dataset: [NovaTech Solutions Company Data.csv](https://github.com/bate-bita/NovaTech-Business-Performance-Dashboard/blob/main/NovaTech%20Solutions%20Company%20Data.csv)

---

## Dashboard Pages

### Page 1: Executive Summary

![Executive Summary](NovaTech%20SAC%20Dashboard%20Screenshots/01-Executive%20Summary.png)

The hero page designed for senior leadership. Answers the question: how is NovaTech performing overall?

**KPI Tiles:**
- Total Gross Profit: $68,660,740 vs planned $67,419,650
- Total Revenue: $165,282,728 vs planned $163,947,020
- Total Cost: $96,621,753 vs planned $96,527,197
- Gross Profit Margin %: 41.54%
- Revenue Variance %: 0.81%
- Cost Variance %: 0.10%
- New Customers: 3,957
- Lost Customers: 1,272

**Charts:**
- Gross Profit by Region: horizontal bar chart showing North America as the strongest region at $23.6M
- Gross Profit by Product Line: horizontal bar chart showing Cloud Solutions as the highest product line at $31.0M
- Revenue by RAG Status: bar chart showing revenue split across Green, Amber and Red performing records

**RAG Status Thresholds:**
- Green: revenue variance greater than 3% vs planned
- Amber: revenue variance between -3% and 3% vs planned
- Red: revenue variance below -3% vs planned

**Key Insights:**
- Total revenue exceeded planned by 0.81% across both years
- Cloud Solutions is the highest gross profit product line at $31.0M
- North America dominates regional gross profit at $23.6M
- Amber status holds the largest revenue share at $69.8M indicating most records sit in the watch-closely zone
- Customer acquisition of 3,957 significantly outpaced customer loss of 1,272

---

### Page 2: Revenue Performance Analysis

![Revenue Performance Analysis](NovaTech%20SAC%20Dashboard%20Screenshots/02-Revenue%20Performance.png)

The analytical depth page designed for managers investigating specific revenue performance gaps.

**Charts:**
- Revenue Variance Heatmap by Region and Product Line: a 4 by 5 grid showing variance percentages for every product line and region combination, color coded from red for underperformance to green for outperformance
- Revenue Variance by Region: horizontal bar chart sorted descending showing which regions drove the most positive variance in USD
- Revenue Variance by Product Line: horizontal bar chart showing which product lines drove the most positive variance in USD
- Revenue vs Gross Margin by Region: bubble chart with Revenue Actual on the X axis, Gross Margin % on the Y axis, Headcount as bubble size, and Region as color

**Key Insights:**
- North America generated the highest positive revenue variance at $757,472
- Latin America generated the lowest positive revenue variance at $23,941
- North America Professional Services at 3.20% was the strongest outperformer in the heatmap
- Hardware consistently underperformed across multiple regions
- Data and Analytics drove the highest absolute revenue variance by product line at $469,812

---

### Page 3: Cost Performance Analysis

![Cost Performance Analysis](NovaTech%20SAC%20Dashboard%20Screenshots/03-Cost%20Performance.png)

The cost efficiency page designed for finance teams monitoring spending against plan.

**Charts:**
- Cost Variance Heatmap by Region and Product Line: a 4 by 5 grid showing cost variance percentages, color coded from red for overspend to green for underspend
- Cost Variance by Region: diverging bar chart showing which regions overspent or underspent vs plan
- Cost Variance by Product Line: diverging bar chart showing which product lines overspent or underspent vs plan
- Actual vs Planned Cost by Region: clustered bar chart showing Cost Actual vs Cost Planned side by side for all 5 regions

**Cost Variance Logic:**
- Negative variance = underspend vs plan
- Positive variance = overspend vs plan

Note: underspend is not always favorable. It can reflect strong cost discipline but may also indicate underutilized budgets, delayed projects, or missed investment opportunities. Context matters when interpreting cost variance.

**Key Insights:**
- Cloud Solutions overspent by $191,787, the largest cost overrun by product line
- Professional Services underspent by $91,399, the strongest cost efficiency by product line
- North America overspent by $114,833 at the regional level
- Latin America underspent by $44,021 at the regional level
- Most regions tracked very closely to planned cost, suggesting either strong budget discipline or conservative planning assumptions worth investigating further

---

### Page 4: Profitability Performance Analysis

![Profitability Performance Analysis](NovaTech%20SAC%20Dashboard%20Screenshots/04-Profitability%20Performance.png)

The margin analysis page showing how efficiently NovaTech converts revenue into profit across regions and product lines.

**Charts:**
- Gross Profit Margin % Heatmap by Region and Product Line: showing margin percentages for every combination, all cells in green indicating healthy margins across the board
- Gross Profit by Region: horizontal bar chart showing North America at $23.6M
- Gross Profit by Product Line: horizontal bar chart showing Cloud Solutions at $31.0M
- Gross Profit vs Gross Margin by Region: bubble chart with Gross Profit Actual on the X axis, Gross Margin % on the Y axis, Headcount as bubble size, and Region as color

**Key Insights:**
- Cloud Solutions achieved the highest gross margin at 47-48% consistently across all regions
- Hardware had the lowest gross margin at 27-29% reflecting physical product cost structures
- North America generated the highest gross profit volume at $11M with approximately 45% margin
- Latin America's challenge is revenue volume, not margin efficiency
- Gross margins remained stable across all regions and product lines indicating consistent cost management

---

### Page 5: Year Over Year Trends

![Year Over Year Trends](NovaTech%20SAC%20Dashboard%20Screenshots/05-Year%20over%20Year%20Trends.png)

The time series page showing how NovaTech performed over 24 months and whether the business improved year over year.

**Charts:**
- Monthly Revenue vs Cost Trend 2023-2024: line chart showing Revenue Actual and Cost Actual across all 24 months
- Quarterly Gross Profit Performance 2023 vs 2024: grouped bar chart showing Q1 through Q4 side by side for both years
- Monthly Cost Performance Actual vs Planned: line chart showing cost tracking against plan across 24 months
- Net Customer Movement by Month: line chart showing new customers and lost customers each month across both years

**Key Insights:**
- Revenue grew consistently from 2023 to 2024 with Q4 2024 reaching $9.9M vs Q4 2023 at $8.7M
- Every single quarter in 2024 outperformed the equivalent quarter in 2023
- Cost tracked closely to plan across all 24 months indicating strong budget discipline
- New customers consistently outnumbered lost customers in every single month across both years
- July 2023 recorded the lowest net customer movement at 61, a notable dip worth investigating
- Customer acquisition peaked in mid 2024 reaching 201 new customers in a single month

---

## Dataset Structure

The dataset was generated using Python with realistic business logic including seasonal patterns, year-over-year growth of 12%, and a natural distribution of performance outcomes.

**Dimensions:** Date, Year, Month, Quarter, Region, Country, Product Line, Product Category, RAG Status, Currency

**Measures:** Revenue Actual, Revenue Budget, Revenue Variance, Cost Actual, Cost Budget, Cost Variance, Gross Profit Actual, Gross Profit Budget, Gross Profit Variance, Gross Margin Actual %, Gross Margin Budget %, Headcount, New Customers, Lost Customers, Sales Rep Count

**Calculated Measures built in SAC Modeler:**
- CM_Revenue_Variance_Pct: Revenue Actual divided by Revenue Budget minus 1
- CM_Cost_Variance_Pct: Cost Actual divided by Cost Budget minus 1
- CM_Gross_Margin_Pct: Gross Profit Actual divided by Revenue Actual
- CM_Net_Customer_Movement: New Customers minus Lost Customers
- CM_Variance_Index: Revenue Actual divided by Revenue Budget, used for heatmap color scaling

---

## Technical Challenges and How They Were Solved

### Challenge 1: Heatmap color scale with negative values
SAC's gradient palette does not accept negative numbers in the color scale settings. The goal was to show negative variance as red, near zero as neutral, and positive variance as green. Every attempt to input negative minimum values was rejected with an ascending order error.

**Solution:** First attempted to solve this by creating a calculated measure called CM_Variance_Index dividing Revenue Actual by Revenue Budget to produce only positive values, but this did not fully resolve the color mapping issue. The final solution was to keep the variance percentage values directly and instead tweak the gradient color intervals, shift the midpoint position from 50% to 70% to compress the neutral zone, and replace the harsh red with a softer tone. This required iterative experimentation but produced a clean and accurate color scale that correctly communicates underperformance and outperformance across the heatmap.

### Challenge 2: Month ordering in filter dropdown
The month filter panel dropdown was sorting alphabetically rather than chronologically, displaying Apr, Aug, Dec, Feb, Jan instead of Jan, Feb, Mar.

**Solution:** Manually reordered the Month dimension through the dimension filter settings in SAC to restore proper calendar chronology in the filter panel.

### Challenge 3: Dual axis chart with incompatible scales
An attempt was made to layer Revenue and Gross Margin Percentage on a single dual axis line chart. While SAC supports dual axis charts technically, the visual result was unclear because revenue values in the millions and margin percentages in the forties appeared on incompatible scales that confused the narrative.

**Solution:** Split into two separate focused charts. Two clean focused charts communicate more clearly than one overloaded chart.

### Challenge 4: Headcount aggregation error on scatter plot
When building the Cost vs Gross Margin scatter plot, the chart displayed values of 19, 25, 9, 11, and 33 instead of the expected millions-level cost figures. The chart was counting records rather than summing cost values due to residual configuration settings carried over from a previous bubble chart that used Headcount as its size measure.

**Solution:** Deleted the chart entirely and rebuilt it from scratch without carrying over any previous configuration. The rebuilt chart correctly aggregated Cost Actual and Cost Planned as SUM measures and displayed accurate values in the tens of millions.

### Challenge 5: Table chart configuration
SAC's table chart type requires dimensions in rows and measures in columns using a specific drag and drop workflow that is not immediately intuitive. Initial attempts produced a single cell table showing only a default measure.

**Solution:** Replaced the table entirely with a grouped bar chart showing Quarterly Gross Profit Performance by year. This delivered the same quarterly comparison story in a more visually impactful format.

---

## Tools and Techniques

- **Platform:** SAP Analytics Cloud, Story Builder with Canvas layout
- **Data Generation:** Python with CSV output, structured to match SAC Modeler requirements
- **Modeler Setup:** Custom dimensions, semantic type assignments, calculated measures using RESTRICT style logic and arithmetic formulas
- **Analytical Skills Demonstrated:** Actuals vs budget variance analysis, gross margin analysis, RAG performance framework, regional performance benchmarking, year-over-year trend analysis, customer movement tracking, executive dashboard design, cost efficiency analysis.

---

## Key Business Story

NovaTech Solutions delivered solid performance over the 2023 to 2024 period. Revenue exceeded planned by 0.81% overall, growing consistently quarter over quarter across both years. Cloud Solutions and Data and Analytics drove the highest revenue and margins. North America was the strongest region across revenue, cost efficiency, and gross profit while Latin America consistently underperformed on volume but not on margin efficiency. Gross margins remained stable between 39% and 44% throughout both years indicating healthy cost management despite revenue growth. Customer acquisition consistently outpaced customer loss in every single month across both years, and Cloud Solutions maintained gross margins of 47-48% across all five regions without exception.

---

## Author

**Bate Bita Tambe**  
Data Analyst 

[LinkedIn](https://www.linkedin.com/in/bate-bita-tambe) 
