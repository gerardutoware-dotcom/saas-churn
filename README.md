# SaaS Customer Retention and Revenue Risk Diagnostic

## Executive Summary
This project provides an end-to-end analytical solution for a subscription-based SaaS business to combat customer churn. By bridging the gap between raw activity logs and executive strategy, this dashboard identifies high-value revenue at risk and provides Customer Success teams with a prioritized Action List for immediate outreach.

### Key Business Insights
* The Engagement Gap: Analysis revealed that Critical Risk accounts have a 40% lower engagement ratio compared to healthy accounts.
* Support Paradox: High ticket volume combined with low active hours was identified as the strongest predictor of churn.
* Revenue Concentration: The AMER Enterprise segment currently holds the highest concentration of revenue at risk.

---

## Technical Data Stack
* Python (Google Colab): Synthetic data generation and Exploratory Data Analysis (EDA).
* SQL (Google BigQuery): Large-scale data transformation and account health logic.
* Tableau: Interactive BI dashboarding and operational reporting.

---

## Project Lifecycle and Methodology

### 1. Data Engineering (Python)
Generated a synthetic dataset to simulate real-world SaaS behaviors.
* Caption: Utilized Pandas to generate features such as Monthly Rate, Active Hours, and Support Ticket volume, ensuring realistic correlations for churn modeling.

### 2. Diagnostic Analysis (BigQuery SQL)
Calculated the Engagement Ratio—a custom metric balancing product usage against support overhead.
* Caption: Engineered a Value-per-Ticket metric to identify friction points where customers are struggling with the platform.

### 3. Segmentation Logic
Developed a logic-based Account Health Status classifier using SQL CASE statements to prioritize retention efforts:
* Critical Risk: Low Engagement + High Annual Contract Value (ACV).
* At-Risk: Declining activity over a 30-day period.
* Healthy: High usage-to-ticket ratio.

---

## Dashboard Implementation
The final Tableau dashboard features a high-to-low design flow for different stakeholders:
1. Strategic Layer: Top-level KPIs showing Total Revenue at Risk.
2. Diagnostic Layer: Tree Map showing risk concentration by Region and Plan.
3. Operational Layer: A dynamic Action List for Account Managers to identify specific Customer IDs.

[[Link to Interactive Tableau Public Dashboard](https://public.tableau.com/app/profile/gerard.utoware7696/viz/ProjectWork1_17677435337750/TotalRevenueatRisk)]

---

## Project Reflection
A primary challenge was avoiding the Aggregation Trap. Initial global averages masked the severity of specific segment failures. By pivoting to Weighted Averages and implementing Dashboard Action Filters, I transformed noisy data into a tool that allows a user to move from a global trend to a specific customer ID in exactly two clicks.

---
