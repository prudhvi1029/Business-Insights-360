# AtliQ Hardware Business Insights 360 : Power BI Project

This repository serves as my documentation for the AtliQ Hardwares Business Insights 360 - Power BI Project.
It was created as a self-learning project for the course: [Get Job Ready: Power BI Data Analytics for All Levels 2.0](https://codebasics.io/courses/power-bi-data-analysis-with-end-to-end-project) by [Codebasics](https://codebasics.io/).

The entire project has been implemented using Microsoft Power BI Desktop  and published on Microsoft Power BI Service.

The project data files have not been uploaded to this repository in compliance with Codebasics Data & Content Distribution Policy.

---
## Contents:
- [Business Insights 360 Live Report Link](#business-insights-360-live-report-link)
- [Power BI Techniques Learned](#power-bi-techniques-learned)
- [Domain Knowledge](#domain-knowledge)
  - [Business Domains](#business-domains)
  - [Business Related Terms](#business-related-terms)
  - [Sales Channels](#sales-channels)
- [About AtliQ Hardware](#about-atliq-hardware)
- [Problem Statement](#problem-statement)
- [Tools and Technologies Used](#tools-and-technologies-used)
- [About the Dataset](#about-the-dataset)
  - [Data Sources](#data-sources)
- [Data Model](#data-model)
- [Project Implementation](#project-implementation)
- [BI 360 Report Overview](#bi-360-report-overview)
  - [Home View](#i-home-view)
  - [Finance View](#ii-finance-view)
  - [Sales View](#iii-sales-view)
  - [Marketing View](#iv-marketing-view)
  - [Supply Chain View](#v-supply-chain-view)
  - [Executive View](#vi-executive-view)
- [Conclusion](#conclusion)

You can add this Table of Contents section to your `README.md` file to provide clear navigation links for your project documentation.

---

## [Business Insights 360 Live Report Link](https://app.powerbi.com/view?r=eyJrIjoiNTA2Mjg5ZDEtMzNhMi00ODI0LWJmM2EtM2FmNDcwMTYzNWVjIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)

---
## Power BI Techniques Learned

Throughout the development of the AtliQ Hardware Power BI project, several advanced Power BI techniques and functionalities were employed to ensure robust and efficient data handling and visualization:

- **Questions for Project Initiation**: Defined critical questions to be addressed before starting the project to align objectives, data requirements, and stakeholder expectations.
- **Creating Calculated Columns**: Utilized DAX to create calculated columns, enhancing data analysis within the model.
- **Creating Measures Using DAX**: Developed measures using DAX language for dynamic calculations across reports.
  - **CALCULATE()**: Used to perform conditional calculations based on specific criteria.
  - **DIVIDE()**: Applied to safely perform divisions and handle potential errors from zero division.
  - **FILTER()**: Employed to filter data dynamically within formulas.
  - **SWITCH()**: Utilized to simplify complex nested IF conditions for better readability and performance.
- **Data Modeling**: Designed comprehensive data models to establish relationships and facilitate efficient data analysis.
- **Using Bookmarks for Visual Management**: Implemented bookmarks to switch between visuals dynamically, enhancing report interactivity.
- **Page Navigation with Buttons**: Used button-driven navigation to streamline user experiences and report accessibility.
- **Creating Date Tables Using M Language**: Generated custom date tables in M language to support time-based analyses.
- **Dynamic Titles Based on Filters**: Configured visual titles to dynamically adjust based on applied report filters.
- **Using KPI Indicators**: Integrated KPI indicators to visually represent progress towards targets within dashboards.
- **Conditional Formatting**: Applied conditional formatting in visuals using icons or background colors to enhance data readability and focus.
- **Data Validation Techniques**: Implemented robust data validation processes to ensure the accuracy and quality of the data used.
- **Power BI Services**:
  - **Publishing Reports**: Reports were published to Power BI Service to facilitate access across teams.
  - **Setting Up Personal Gateway**: Configured personal gateways for automatic data refresh, ensuring data is current and reliable.
  - **Power BI App Creation**: Developed Power BI apps to consolidate reports and dashboards, simplifying distribution and access.
  - **Collaboration and Permissions**: Managed workspace access and permissions, ensuring secure and role-appropriate access to BI resources
---
## Domain Knowledge

#### Business Domains

- **Finance**: Understanding financial metrics such as Net Profit, Gross Margin, and more.
- **Sales**: Insights into sales performance, tracking direct sales, and distributor metrics.
- **Marketing**: Analysis of marketing efforts and their impact on sales and brand positioning.
- **Supply Chain**: Management of inventory, understanding supply chain logistics and efficiency

#### Business Related Terms

Familiarity with these terms was crucial to accurately interpret data and derive insights:

- **Gross Price**: The total price of products before any deductions.
- **Pre-invoice Deductions**: Discounts or allowances applied before invoicing.
- **Post-Invoice Deductions**: Rebates or penalties applied after invoicing.
- **Net Invoice Sale**: The actual invoiced amount after all deductions.
- **Gross Margin**: The difference between revenue and cost of goods sold, expressed as a percentage of revenue.
- **Net Sales**: Sales after deductions from returned goods.
- **Net Profit**: Profit remaining after all expenses, including COGS and operational expenses.
- **COGC (Cost of Goods Sold)**: Direct costs attributable to the production of the goods sold.
- **YTD (Year to Date)**: A period, starting from the beginning of the current year and continuing up to the present day.
- **YTG (Year to Go)**: The remaining part of the year from the current date to the end of the year.

#### Sales Channels

Understanding different sales channels was essential for analyzing market strategies:

- **Direct**: Selling directly to consumers without any intermediaries.
- **Retailer**: Sales made through retail channels.
- **Distributors**: Third-party distributors who sell products to retailers or directly to consumers.
---
## About AtliQ Hardware:
**Domain:** Consumer Goods | **Functions:** Finance, Sales, Marketing, Supply Chain and Executive

- AtliQ Hardwares is company that sells computer hardware and peripherals like PC, mouse, printer etc. to clients across the world.
- They have a major B2B business model wherein they sell to stores like Croma, Best Buy, Staples, Flipkart etc. who then sell it to the end users (consumers). These stores are their main customers.
- They sell through 3 channels: Retailer, Direct and Distributor.
- AtliQ Hardwares’s Customers are of two types. Both these Platforms are called Retailer channels.
  1. Brick & Mortar Customer: Actual physical stores e.g. Croma, Best Buy
  2. E-commerce Customer: Online websites E.g. Amazon, Flipkart
- AtliQ Hardwares also has a minor B2C business model wherein they own stores: AtliQ E-store and AtliQ Exclusive. These are called Direct channels.
- They also have Distributors in some countries with restricted trade. E.g. Neptune
  
---

## Problem Statement:
AltiQ Hardware, a global leader in computers and accessories, faced unexpected losses after opening a store in America. These setbacks were identified to be caused due to reliance on outdated methods such as Excel for data analysis. To address this issue, the company's leadership recognized the need for a transformative approach to leveraging data for informed decision-making. With competitors boasting robust analytics teams, AltiQ Hardware recognizes the urgent need to develop its analytics capabilities using Power BI to thrive in the industry.

To outshine competitors, they've adopted Power BI for analytics with 1.8 million transaction records from Excel, CSV, and MySQL.

### Step-by-Step Execution: Building the Business Insights 360 DashBoard  

- **Project Charter Implementation**: Establish a clear roadmap and accountability through a well-structured Project Charter.
- **Benchmark-Backed Data Validation**: Ensure high data quality by processing and validating over 1 million rows of data against company benchmarks.
- **Data Modeling Excellence**: Create robust data models using Star and Snowflake Schema methodologies to clarify relationships and data flow.
- **Transforming Data with Power Query**: Utilize Power Query to transform raw data into actionable insights.
- **Optimized Reports for Seamless Insights**: Enhance report navigation and performance, improving the decision-making process.
- **Stakeholder Mapping Analysis**: Identify and analyze key stakeholders to tailor engagement and communication strategies effectively.
- **Finance Insights Unveiled**: Develop a dynamic P&L table structure to provide flexible and comprehensive financial insights.
- **Sales Performance Redefined**: Implement advanced visualizations to depict sales trends and performance metrics dynamically.
- **Marketing Analytics at its Best**: Equip the marketing team with strategic insights through innovative BI tools.
- **Supply Chain Visibility Achieved**: Enhance supply chain efficiency through detailed inventory forecasts and error analysis.
- **Executive Dashboard**: Offer executives a clear view of operational performance and market trends to aid strategic planning.
- **Unleashing the Power of Power BI Services**: Guide the team on utilizing Power BI Services for real-time insights and collaboration.
----
## Tools and Technologies Used
1. **Microsoft Power BI**
    - **Power BI Desktop**: Utilized for creating data models, performing data transformation (ETL), and developing interactive visualizations and dashboards.
    - **Power BI Service:** Used for sharing reports, setting up automated data refreshes, and managing the BI environment in the cloud.
2. **SQL Databases** : Data Storage and Management: Acts as the primary storage for structured data, enabling complex queries and data manipulation for reporting.  
3. **Microsoft Excel**:Data Analysis and Reporting: Employed for preliminary data analysis, manipulation, and as an interim data storage format before importing into Power BI.  
4. **CSV Files**:Data Import and Integration: CSV files are used as a data source for importing historical data and integrating with other data formats.  
5. **GitHub**:Documentation and Version Control: Serves as the repository for all documentation related to the project.
---

## About the Dataset:

### Data Sources:
The dataset contains 11 tables in total, namely:
- **From gdb041 MySQL Server:**
  - dim_customer: 209 records | 5 columns
  - dim_market: 27 records | 3 columns
  - dim_product: 397 records | 6 columns
  - fact_forecast_monthly: 1,885,941 records | 4 columns
  - fact_sales_monthly: 1,885,941 records | 4 columns
- **From gdb041 MySQL Server:**
  - freight_cost: 135 records | 4 columns
  - manufacturing_cost: 1,197 records | 3 columns
  - post_invoice_deductions: 2,063,076 records | 5 columns
- **Excel Files:**
  - market_share: 737 records | 6 columns
  - operational_expense: 113 records | 4 columns
  - ns_gm_target: 321 records | 5 columns
---

### Data Model:
![Screenshot 2025-01-08 100331](https://github.com/user-attachments/assets/4dcde6ac-b592-419f-be09-4464f791ac62)  
![Screenshot 2025-01-08 100355](https://github.com/user-attachments/assets/5244e7f7-c1bb-4de3-8d00-b89f86156e4c)


---

## Project Implementation:
Please find the documentation links for the project phase-wise implementation below:  

Here are the detailed links for every section below the phases in your `Documentation.md`:

- [Phase 1: Data Wrangling](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#phase-1-data-wrangling)
  - [Step 1: Loading Data to MySQL Workbench](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-1-loading-data-to-mysql-workbench)
  - [Step 2: Connecting MySQL Database to Power BI](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-2-connecting-mysql-database-to-power-bi)
- [Phase 2: ETL with Power Query](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#phase-2-etl-with-power-query)
  - [Step 1: Creating custom Date Table](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-1-creating-custom-date-table)
  - [Step 2: Creating Last Sales Month Reference Table](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-2-creating-last-sales-month-reference-table)
  - [Step 3: Creating Remaining Forecast Reference Table](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-3-creating-remaining-forecast-reference-table)
  - [Step 4: Creating a New Table with both Actual & Forecast Data](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-4-creating-a-new-table-with-both-actual--forecast-data)
  - [Step 5: Calculating Net Invoice Sales based on FY varying Gross Price & Pre-invoice Deductions](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-5-calculating-net-invoice-sales-based-on-fy-varying-gross-price--pre-invoice-deductions)
- [Phase 3: Data Modelling & Calculated Columns](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#phase-3-data-modelling--calculated-columns)
  - [Step 1: Normalizing Data in Tables](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-1-normalizing-data-in-tables)
  - [Step 2: Creating Table Relationships](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-2-creating-table-relationships)
  - [Step 3: Creating fiscal_year table using DAX](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-3-creating-fiscal_year-table-using-dax)
  - [Step 4: Calculated Columns for post_invoice Calculations](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-4-calculated-columns-for-post_invoice-calculations)
  - [Step 5: Calculated Columns for COGS & Gross Margin Calculations](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-5-calculated-columns-for-cogs--gross-margin-calculations)
  - [Step 6: Optimizing Report File Size](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-6-optimizing-report-file-size)
- [Phase 4: Finance View](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#phase-4-finance-view)
  - [Step 1: Creating Measures Table](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-1-creating-measures-table)
  - [Step 2: Creating P & L Measures](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-2-creating-p--l-measures)
  - [Step 3: Creating P & L Rows Table](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-3-creating-p--l-rows-table)
  - [Step 4: Building P&L Matrix visual](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-4-building-pl-matrix-visual)
  - [Step 5: Configuring Quarters & YTD/YTG Slicers](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-5-configuring-quarters--ytdytg-slicers)
  - [Step 6: Building P&L Performance over Time visual](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-6-building-pl-performance-over-time-visual)
  - [Step 7: Building Top Market & Product visuals](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-7-building-top-market--product-visuals)
  - [Step 8: Importing Operating Expenses Data](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-8-importing-operating-expenses-data)
  - [Step 9: Calculated Columns & Measures for Operational Expenses & Net Profit Calculations](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-9-calculated-columns--measures-for-operational-expenses--net-profit-calculations)
  - [Step 10: Updating the P&L visual with Operating Expenses and Net Profit](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-10-updating-the-pl-visual-with-operating-expenses-and-net-profit)
- [Phase 5: Sales View](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#phase-5-sales-view)
  - [Step 1: Building Customer Performance visual](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-1-building-customer-performance-visual)
  - [Step 2: Building Customers GM & NS Plot visual](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-2-building-customers-gm--ns-plot-visual)
  - [Step 3: Building Product Performance visual](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-3-building-product-performance-visual)
  - [Step 4: Building Unit Economics visual](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-4-building-unit-economics-visual)
- [Phase 6: Marketing View](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#phase-6-marketing-view)
  - [Step 1: Building Product Performance visual](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-1-building-product-performance-visual)
  - [Step 2: Building Products GM & NS Plot visual](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-2-building-products-gm--ns-plot-visual)
  - [Step 3: Building Unit Economics visual](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-3-building-unit-economics-visual)
  - [Step 4: Building Market Performance visual](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-4-building-market-performance-visual)
- [Phase 7: Supply Chain View](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#phase-7-supply-chain-view)
  - [Step 1: Understanding Key Metrics](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-1-understanding-key-metrics)
  - [Step 2: Creating Supply Chain Measures](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-2-creating-supply-chain-measures)
  - [Step 3: Building Supply Chain visuals](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-3-building-supply-chain-visuals)
- [Phase 8: Designing Effective Dashboard](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#phase-8-designing-effective-dashboard)
  - [Step 1: Building Home View landing page](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-1-building-home-view-landing-page)
  - [Step 2: Upgrading Finance View](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-2-upgrading-finance-view)
  - [Step 3: Adding Key Elements to Finance Dashboard](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-3-adding-key-elements-to-finance-dashboard)
  - [Step 4: Configuring Navigation Bar](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-4-configuring-navigation-bar)
  - [Step 5: Upgrading Supply Chain View](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-5-upgrading-supply-chain-view)
  - [Step 6: Upgrading Sales View](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-6-upgrading-sales-view)
  - [Step 7: Upgrading Marketing View](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-7-upgrading-marketing-view)
  - [Step 8: Incorporating Country level NS, GM & NP Target FY 2022 Data in Finance View](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-8-incorporating-country-level-ns-gm--np-target-fy-2022-data-in-finance-view)
  - [Step 9: Updating Finance View visuals](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-9-updating-finance-view-visuals)
  - [Step 10: Creating a Dynamic Switch to toggle between LY and Target benchmarks](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-10-creating-a-dynamic-switch-to-toggle-between-ly-and-target-benchmarks)
  - [Step 11: Configuring BM instead of LY for other Finance View visuals](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-11-configuring-bm-instead-of-ly-for-other-finance-view-visuals)
  - [Step 12: Setup Dynamic GM% Parameter Slicer](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-12-setup-dynamic-gm-parameter-slicer)
  - [Step 13: Configure Toggle Button to switch GM % and NP % in Marketing View Performance Plot visual](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-13-configure-toggle-button-to-switch-gm--and-np--in-marketing-view-performance-plot-visual)
  - [Step 14: Implement custom Tooltip to show NS $ and GM % Trend in Sales View](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-14-implement-custom-tooltip-to-show-ns--and-gm--trend-in-sales-view)
  - [Step 15: Fix Data Quality Issues](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-15-fix-data-quality-issues)
  - [Step 16: Create Support View](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-16-create-support-view)
  - [Step 17: Create Info View](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-17-create-info-view)
  - [Step 18: Save DAX Studio Metrics File](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-18-save-dax-studio-metrics-file)
- [Phase 9: Executive View](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#phase-9-executive-view)
  - [Step 1: Importing Market Share Data](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-1-importing-market-share-data)
  - [Step 2: Configure the Data Model](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-2-configure-the-data-model)
  - [Step 3: Building Market Share View Visuals](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-3-building-market-share-view-visuals)
  - [Step 4: Creating the Executive View](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-4-creating-the-executive-view)
  - [Step 5: Creating Executive KPI Cards](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-5-creating-executive-kpi-cards)
  - [Step 6: Creating Revenue (NS) by Division & Channel Donut Charts](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-6-creating-revenue-ns-by-division--channel-donut-charts)
  - [Step 7: Creating Key Insights by Sub Zone Matrix visual](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-7-creating-key-insights-by-sub-zone-matrix-visual)
  - [Step 8: Creating Yearly Trend Chart](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-8-creating-yearly-trend-chart)
  - [Step 9: Creating Market Share Ribbon Chart Visual](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-9-creating-market-share-ribbon-chart-visual)
  - [Step 10: Creating Top 5 Customers & Products by Revenue Visuals](https://github.com/prudhvi1029/Business-Insights-360/blob/main/Documentation/Documentation.md#step-10-creating-top-5-customers--products-by-revenue-visuals)


---

## BI 360 Report Overview:[Live Report Link](https://app.powerbi.com/view?r=eyJrIjoiNTA2Mjg5ZDEtMzNhMi00ODI0LWJmM2EtM2FmNDcwMTYzNWVjIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)


### I. Home View:

Central navigation hub with easy access to all views, complete with support and information manual.
![Home Page](https://github.com/user-attachments/assets/3dd2e04f-e582-40c0-9fc7-cfb22a1def9a)



### II. Finance View:

Enhances financial planning and cost control, featuring a P&L Statement, Net Sales Trend and Breakdown by Products/Customers and more.

![Finance View](https://github.com/user-attachments/assets/f01d1ffd-a013-46e9-9c90-a499323672d6)


### III. Sales View:

Focuses on boosting sales revenue and tracking customer performance, including Gross Margin % Variance across Customers/Products and more.

![Sales View](https://github.com/user-attachments/assets/93ae3d19-7bff-4d14-afbb-4bc24eaa5c5b)


### IV. Marketing View:

Elevates brand visibility and evaluates marketing campaign ROI, with insights into Segment Performance, Net Profit % Variance across Regions and more.

![Marketing View](https://github.com/user-attachments/assets/4efe51cf-1b2e-4e98-b0d5-7b7b8c7957af)


### V. Supply Chain View:

Optimizes inventory management and demand forecasting, featuring trends in Forecast Accuracy and Inventory Stock Risk by Customers/Products.

![Supply Chain View](https://github.com/user-attachments/assets/940d196b-fd85-4c1d-9cd9-49b1c4ebe045)

### VI. Executive View:

Provides a high-level overview of organizational performance for top AtliQ executives and senior management, showcasing business KPIs, Revenue Contributions by Division/Channel, Top Customers & Products, AtliQ's Market Share Trend and more.

![Executive View](https://github.com/user-attachments/assets/0b10dc08-e362-479d-ac2d-74d9298e3c08)


---

## Conclusion:
The Power BI Report project for AtliQ Hardware provided a comprehensive, data-driven analysis across five critical business functions: Finance, Sales, Marketing, Supply Chain, and Executive. By integrating key business metrics such as Net Sales, Gross Margin, COGS, Net Profit % and Forecast Accuracy % the dashboard offers a holistic view of AtliQ's performance.

The insights gained from this analysis revealed areas of interest, such as robust sales performance and precise forecast accuracy, as well as areas of opportunities for improvement in weak profit margins and supply chain efficiency. Through interactive visualizations and detailed metrics, the dashboard empowers Atliq Hardware's leadership to make informed, strategic decisions that align with their business goals.

---
