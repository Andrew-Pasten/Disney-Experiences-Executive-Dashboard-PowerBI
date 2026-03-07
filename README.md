# Disney Experiences Operations Finance Dashboard (Power BI)

---

## Background and Overview

The Disney Experiences segment represents one of the most operationally complex and financially significant divisions of The Walt Disney Company, encompassing theme parks, resorts, and hospitality operations. Managing performance across business units requires continuous monitoring of revenue generation, operating efficiency, and cost structure to understand the underlying drivers of financial performance.

This project simulates an **Operations Finance and Revenue Management reporting workflow**, replicating how FP&A teams monitor business performance and identify operating income drivers across business units. Using a structured financial dataset and executive-style reporting approach, this dashboard enables real-time analysis of key operational and financial metrics, including:

- Revenue and YoY revenue growth  
- Operating margin and operating income changes  
- Labor cost pressure and labor efficiency  
- Revenue per guest and cost per guest trends  
- Business unit–level profitability variance  

The goal of this project is to demonstrate how finance teams use data visualization, variance analysis, and driver decomposition to explain financial performance and support executive decision-making.

---

## Executive Summary

Analysis of Disney Experiences performance reveals several important financial and operational trends:

- Total segment revenue reached approximately **$24.7B**, with operating margin stabilizing at **26.6%**, indicating strong overall profitability despite cost pressures.  
- Operating income increased by approximately **+$516.6M year-over-year**, driven primarily by revenue expansion of approximately **+$660M**, partially offset by labor cost increases of approximately **−$410M**.  
- Labor costs represented approximately **26.0% of revenue**, highlighting labor efficiency as a critical driver of profitability across business units.  
- Revenue per guest averaged approximately **$750.79**, while cost per guest averaged approximately **$550.73**, reinforcing the importance of operational efficiency and pricing optimization.  
- Business unit–level performance varied significantly. Disneyland Park generated approximately **$11.7B in revenue at 27.2% operating margin**, while Resort Hotels operated at lower margins, reflecting structural differences in cost models and operational leverage.  

These findings mirror real-world Operations Finance workflows, where teams focus on revenue growth sustainability, cost structure efficiency, and drivers of operating income changes.

---

## Dashboard Overview

### 1) Executive Performance Overview

The Executive Overview dashboard provides a high-level summary of financial and operational performance across Disney Experiences business units.

**Key features:**
- Dynamic KPI cards displaying Revenue, Revenue YoY %, Operating Margin %, Labor % of Revenue, Revenue per Guest, and Cost per Guest  
- Trend visualizations tracking operating margin and revenue versus labor cost over time  
- Business Unit and Fiscal Year slicers enabling performance comparison across segments  
- Executive Insight callout summarizing financial performance in a concise finance narrative  

![Executive Overview](screenshots/executive-overview.png)

This page is designed to function like an executive review view: quickly surfacing segment performance, highlighting cost structure trends, and enabling drilldown by business unit.

---

### 2) Drivers Deep Dive (Variance Bridge Analysis)

The Drivers Deep Dive page provides a financial bridge explaining the change in operating income year-over-year.

Using a waterfall chart, operating income changes are decomposed into:
- Revenue Change  
- Labor Cost Change  
- Other Operating Expense Change  
- Net Operating Income Change  

This analysis replicates core FP&A workflows used in corporate financial reporting to isolate profitability drivers.

![Drivers Deep Dive](screenshots/drivers-deep-dive.png)

The FY2025 vs FY2024 operating income bridge shows that operating income improved by approximately **+$516.6M**, driven by strong revenue growth but partially offset by labor cost pressure. This type of bridge helps finance teams explain *why* earnings changed, not just *what* changed.

---

## Business Unit Drilldown Examples

### Disneyland Park – FY2025

Disneyland Park generated approximately **$11.7B in revenue** with **2.4% YoY growth** and a **27.2% operating margin**, reflecting strong operational leverage and healthy profitability at the flagship park business unit.

![Disneyland Park Drilldown](screenshots/disneyland-park-drilldown.png)

This view highlights how the dashboard supports business-unit level analysis, allowing leadership to assess segment-specific margin trends, guest economics, and labor intensity.

---

### Downtown Disney District – FY2024 Contrast Case

Downtown Disney District provides a useful contrast case. In FY2024, revenue declined by **−3.2% YoY**, yet the business still delivered a **38.1% operating margin**, suggesting strong cost control and resilience despite top-line softness.

![Downtown Disney FY2024](screenshots/downtown-disney-fy2024.png)

Including a contrasting case helps demonstrate that the dashboard is not limited to one growth story; it can also surface examples of margin resilience, cost discipline, and structural profitability differences across business units.

---

## Data Structure Overview

The dashboard is built using a **star schema data model**, consistent with enterprise financial reporting environments.

### Fact Table  
**Fact_WeeklyOps**
- Fiscal Year  
- Week Start Date  
- Revenue  
- Labor Cost  
- Other Operating Expense  
- Operating Income  
- Attendance  
- Revenue per Guest  
- Cost per Guest  

This table represents operational and financial performance metrics at the business unit and weekly level.

### Dimension Tables

**Dim_Date**
- Date  
- Fiscal Year  
- Fiscal Quarter  
- Fiscal Month  

Used for time intelligence, trend analysis, and YoY comparisons.

**Dim_BusinessUnit**
- Business Unit Name  
  - Disneyland Park  
  - Disney California Adventure  
  - Disneyland Resort Hotels  
  - Downtown Disney District  

Used to analyze performance across operational segments.

This structure supports advanced measures such as YoY variance analysis, rolling averages, and dynamic executive reporting.

---

## Key Insights Deep Dive

### Revenue Growth Driving Profitability
Revenue growth was the primary driver of operating income expansion, contributing approximately **+$660M year-over-year**. This indicates sustained demand strength and effective revenue management.

### Labor Cost Pressure Moderating Margin Expansion
Labor costs increased by approximately **−$410M**, partially offsetting revenue gains. Labor represented approximately **26% of revenue**, highlighting labor efficiency as a critical operational lever.

### Strong Operational Leverage at Core Park Operations
Disneyland Park generated approximately **27.2% operating margin**, reflecting higher operational leverage and fixed-cost efficiency. Resort Hotels exhibited lower margins, consistent with a different cost structure.

### Margin Resilience in Lower-Revenue Units
Downtown Disney District maintained margins near **38–40%** despite comparatively modest revenue levels, illustrating how cost structure and operating discipline can preserve profitability even when top-line growth is limited.

---

## Recommendations

Based on the analysis, several Operations Finance actions emerge:

- Monitor labor cost growth, as labor cost increases remain the primary offsetting factor against revenue-driven margin expansion.  
- Improve cost per guest through operational efficiency initiatives, particularly within lower-margin business units such as Resort Hotels.  
- Track business unit profitability variance to identify best practices and opportunities for efficiency improvement.  
- Continue using driver-based reporting to isolate operating income changes and support executive decision-making.  

---

## Technical Implementation

This dashboard was developed using:
- **Power BI Desktop**
- **Star schema data modeling**
- **Advanced DAX measures**, including:
  - YoY revenue and operating income changes  
  - Operating margin and labor ratio calculations  
  - Financial bridge logic using `SWITCH()` measures  
  - Time intelligence functions  
  - Dynamic executive titles and insight measures  
  - Rolling averages (4-week moving average)

The project was designed to simulate internal FP&A-style reporting by combining executive-level KPI presentation with dynamic drilldown and driver-based profitability analysis.

---

## Assumptions and Caveats

- The dataset used in this project is **synthetic** and designed to simulate a realistic financial reporting environment.  
- Metrics and performance patterns are structured to reflect plausible business dynamics but do **not** represent actual Disney internal financial results.  
- The goal is to demonstrate financial analysis, dashboard design, and executive reporting capabilities aligned with Operations Finance workflows.  

---

## Links

- GitHub: [Andrew-Pasten](https://github.com/Andrew-Pasten)  
- LinkedIn: [andrewpastencpp](https://www.linkedin.com/in/andrewpastencpp/)  
- Portfolio: [andrew-pasten.github.io](https://andrew-pasten.github.io/Portfolio.io/index.html)
