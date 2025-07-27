# Business Insights 360 - Power BI Project

## Table of Contents

1. [Project Overview](#project-overview)
2. [Company Background](#company-background)
3. [Tech Stack](#tech-stack)
4. [Power BI Techniques Learned](#power-bi-techniques-learned)
5. [Dataset Understanding](#dataset-understanding)
6. [Data Modeling](#data-modeling)
7. [Dashboard Design](#dashboard-design)
8. [Key DAX Measures](#key-dax-measures)
9. [Project Outcome](#project-outcome)
10. [Live Report & Files](#live-report--files)

---

## Project Overview

AtliQ Hardware, a rapidly growing global company, recently suffered a significant loss after expanding into the American market based on intuition and limited Excel-based analysis. To prevent such missteps in the future and remain competitive, the company decided to build a robust data analytics infrastructure using Power BI.

The goal of this project is to empower different departments—Finance, Sales, Marketing, and Supply Chain—with interactive dashboards that enable data-driven decision-making.

---

## Company Background

**AtliQ Hardware** sells computer and computer accessories via three channels:

* Retailers
* Direct
* Distributors

They operate in over 27 markets globally. This project kickstarted the company's first steps toward data-driven analytics.

---

## Tech Stack

**Languages & Tools:**

* SQL
* Power BI Desktop
* Excel
* DAX
* DAX Studio

**Data Management:**

* MySQL for database connectivity

---

## Power BI Techniques Learned

### Data Preparation

* Asking the right stakeholder questions before starting
* Data validation techniques
* Creating calculated columns
* Creating a custom date table using M Language

### Data Modeling

* Snowflake schema
* Creating relationships between fact and dimension tables

### DAX & Calculations

* Measures using DAX
* Use of `DIVIDE()` to avoid zero division errors
* KPI indicators
* Dynamic titles and filter context-based calculations

### Report Design & Publishing

* Bookmarking and navigation with buttons
* Conditional formatting with icons and colors
* Power BI Service publishing
* Setting up a personal gateway for auto-refresh
* Power BI App creation, access control, and workspace collaboration

---

## Dataset Understanding

### gdb041

* **dim\_customer**: 75 customers, 27 markets, platforms (E-commerce, Brick & Mortar), and 3 channels
* **dim\_market**: 27 markets, 7 sub-zones, 4 regions (APAC, EU, LATAM, etc.)
* **dim\_product**: 14 categories across 3 divisions: P\&A, PC, N\&S
* **fact\_forecast\_monthly**: Forecasted quantities for warehouse planning
* **fact\_sales\_monthly**: Actual monthly sales data

### gdb056

* **freight\_cost**: Travel and shipping costs
* **gross\_price**: Product pricing
* **manufacturing\_cost**: Cost of goods sold
* **pre\_invoice\_deductions** & **post\_invoice\_deductions**: Discounts and deductions by customer and year

---

## Data Modeling

A Snowflake schema was used for efficient analytical performance.

---

## Dashboard Design

The dashboard was designed based on stakeholder mockups and includes:

* **Home Page** with navigation buttons
* **Finance View**
* **Sales View**
* **Marketing View**
* **Supply Chain View**
* **Executive View**
* **Product Insights**
* **Support Page**

### Dashboard GIF Previews
## Home page
[Home page](https://github.com/SubhajitRoyom/Business-Insights-360/blob/main/Home%20page.png)

## Finance View
![Finance view]

## Sales view
![Sales view]

## Marketing view
![Marketing view]

## Supplychain view
![Supplychain view]

## Executive view
![Executive view]
---

## Key DAX Measures

* `Total Net Sales = [Gross Sales] - [Pre Invoice Deductions] - [Post Invoice Deductions]`
* `Gross Margin % = DIVIDE([Net Sales] - [COGS], [Net Sales])`
* `Forecast Accuracy % = DIVIDE([Forecast Qty] - [Actual Qty], [Forecast Qty])`
* `YTD Sales = TOTALYTD([Net Sales], 'Date'[Date])`
* `Top Product by Market = RANKX(ALL('Product'), [Net Sales])`

---

## Project Outcome

With this dashboard:

* Executives get an overview of performance across departments
* Finance can track profitability and margins
* Marketing can identify top-performing regions and platforms
* Supply chain teams can evaluate forecast accuracy vs actuals
* Sales can monitor monthly and yearly growth

This project empowered AtliQ Hardware to base their decisions on actual data, reducing risk and improving efficiency across the organization.

---

## Live Report & Files

* 🔗 [Live Report]()
* 📂 [PBIX Report File on GitHub]()

---

Feel free to connect with me on [LinkedIn]

---
