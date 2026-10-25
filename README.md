# 📊 Business Insights 360 – Executive & Operational Analytics

[![Power BI](https://img.shields.io/badge/Power_BI-Desktop_%26_Service-F2C94C?logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![SQL](https://img.shields.io/badge/Database-MySQL-4479A1?logo=mysql&logoColor=white)](https://www.mysql.com/)
[![Git LFS](https://img.shields.io/badge/Git-LFS_Enabled-F05032?logo=git&logoColor=white)](https://git-lfs.github.com/)

---

## 🔗 Quick Links
* 🚀 **[Live Interactive Dashboard](#)** *([Link](https://app.powerbi.com/view?r=eyJrIjoiNDgzYjBkNDctOTI0Zi00NTM1LWEwODQtYTA3ZmFjMzE0NWVkIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9))*

---

## 📌 Project Overview & Context

**AtliQ Hardware** is a fast-growing global manufacturer selling computers and accessories through three primary channels: **Retailers**, **Direct**, and **Distributors** across physical store (*Brick & Mortar*) and *E-Commerce* platforms.

After experiencing unexpected market losses due to expanding into new territories based on static intuition and spreadsheet analysis, AtliQ leadership initiated **Business Insights 360**. This Power BI solution transitions the business from intuition-based decision-making to an automated, data-driven analytics culture across **Finance, Sales, Marketing, and Supply Chain**.

---

## 🛠️ Tech Stack & Tools

* **Business Intelligence:** Power BI Desktop, Power BI Service (Workspaces, Apps, Gateways)
* **Database & Querying:** MySQL Workbench (Relational Database Import)
* **Analytics & Calculations:** DAX (Data Analysis Expressions), M Language (Custom Date Tables)
* **Optimization & Data Engineering:** DAX Studio
* **Project Management:** Project Charter, Stakeholder Alignment Framework

---

## PowerBI techniques Learnt

- What are all the questions should be asked before staring the project
- Creating calculated columns
- creating measure using DAX language
- Data modeling
- Using Bookmarks to switch between two visuals
- Page navigation with buttons
- Using divide function to prevent zero division errors
- creating date table using m language
- Dynamic titles based on the applied filters
- Using KPI indicators
- Conditional formatting the values in visuals using icons or background color
- Data validation techniques
- PowerBi services
- Publishing reports to PowerBi services
- Setting up personal gateway to set up the auto refresh of data
- PowerBi App creation
- Collaboration, workspace, access permissions in PowerBi services

---

Project kick off session, where you should get clear of for what and why this project and all other questions you have with regards to the project

### Questions to ask before starting with dashboard

- What is the objective of building this PowerBi dashboard?
- In what terms the success of this project will be measured?
- What will be time dead-line of the project?
- do the stakeholders expecting pre-view before the actual release?
- What are all the hopes stakeholders have out of this project?
- what are all fears the stakeholder have in terms of building this dashboard?
- Who are all will be using this dashboard and for what purpose?
- what are all expectation the stakeholders have, by the completion of this project?
- What can go wrong while building this project?
- what are all the resources/ data needed to build this dashboard?
- is there any inputs from stakeholders in terms of design and views of the dashboard?

After the project kick off meetings, the data engineering team has given the data as per the request of data analytics team, let’s explore them.

---

## 🗄️ Data Architecture & Modeling

The project integrates data from two MySQL databases (`gdb041` and `gdb056`) organized into a high-performance **Snowflake Schema** to balance normalization and analytical speed.

Understanding what data is available will be more helpful while doing analysis. before jumping on to the analysis get good understanding of what are data available.

Dimension table : It will have the static data like details of customer and products

Fact table : It will have the data about the transactions  

- gdb041:
    - dim_customer
        - **27** distinct markets (ex India, USA, spain)
        - **75** distinct customers thorough out the market
        - **2** types of platforms
            - Brick & Motors - Physical/offline store
            - E-commerce - Online Store (Amazon, flipkart)
        - Three channels
            - Retailer
            - Direct
            - Distributors
    - dim_market
        - **27** distinct markets (ex India, USA, spain)
        - 7 sub-zones
        - 4 regions
            - APAC
            - EU
            - nan
            - LATAM
    - dim_product
        - Divisions
            - P & A
                - Peripherals
                - Accessories
            - PC
                - Notebook
                - Desktop
            - N & S
                - Networking
                - Storage
        - There are 14 different categories, Like Internal HDD, keyboard
        - There are different variants available for the same product
    - fact_forecast_monthly
        - This table is used to forecast the customer’s need in advance, which can help in
            - Higher customer satisfaction
            - Reduced cost in warehouses for storage purpose
        - The table is denormalized by data engineering team, as it is a data warehouse which is aimed to be used for analytical work.
        - All the date of the month will be replaced by the start date of the month
        - It will have all the column names and in the end it will have the forecast quantity need of the customer
    - fact_sales_monthly
        - This table is more or less is same as fact_forecase_monthly table, but the last column has the value of sold quantity instead of forecast value.
- gdb056
    - freight_cost
        - This table has details of travel cost and other cost for each market with fiscal year
    - gross_price
        - Has the details of gross prices with product code
    - manufacturing_cost
        - Has the details of manufacturing cost with product code with year
    - Pre_invoice_dedutions
        - Has the details of pre invoice deductions percentage for each cutomer with year
    - Post_invoice_deductions
        - Post invoice deductions and other deductions details

## Importing data into PowerBi

- As the database is MySQL in this project, we need to import the datasets from Mysql database to PowerBi by providing the Database access credential

## Data Model

- Data modeling plays a vital role and is considered as the basement of report. All the visuals will be build upon the data model.
- Poor data modeling affects the over all performance of the report.
- Following Good practices of data modeling is must. Refer this page to get to know the good practices [Blog](https://addendanalytics.com/blog/data-modelling-best-practices/)
- In this project, we have followed Snowfall data modeling method.

<img src="https://github.com/desh-akhil156/Business_Insights_360/blob/main/Resources/Data_model.png" class="center">

### Dashboard designing

Based on the mock ups received as requirement, the team will start designing the visuals and create measure as and when required

## 📈 Executive & Departmental Dashboard Views

The interactive dashboard is organized into dedicated functional modules:

| Dashboard View | Focus Area & Key Metrics |
| :--- | :--- |
| **🏠 Home View** | Central navigation hub with single-click routing to all departmental reports. |
| **💰 Finance View** | Profit & Loss (P&L) statements, Net Sales, Gross Margin %, and COGS benchmark tracking. |
| **🛍️ Sales View** | Top/Bottom customer performance, net sales variance, and regional unit distribution. |
| **📣 Marketing View** | Product category performance, channel profitability, and market-level ROI. |
| **📦 Supply Chain View** | Forecast Accuracy %, Net Error, and inventory bottleneck mitigation. |
| **👑 Executive View** | High-level summary of consolidated revenue, market share trends, and top N insights. |

---


## Home view

In Home view, all the views button will be available. User will land on specific view page by clicking the button 

- Info
- Finance View
- Sales View
- Marketing View
- Supply chain View
- Executive View
- Products
- Support

![Home.png](https://github.com/desh-akhil156/Business_Insights_360/blob/main/Resources/Home_Page.png)

## Finance View

![Finance_view.png](https://github.com/desh-akhil156/Business_Insights_360/blob/main/Resources/Finance_view.png)
## Sales View

![Sales_view.png](https://github.com/desh-akhil156/Business_Insights_360/blob/main/Resources/Sales_view.png)

## Marketing View

![Marketing_view.png](https://github.com/desh-akhil156/Business_Insights_360/blob/main/Resources/Marketing_view.png)

## Supply chain View

![Supply Chain_view.png](https://github.com/desh-akhil156/Business_Insights_360/blob/main/Resources/Supply_Chain_view.png)

## Executive View

![Executive_view.png](https://github.com/desh-akhil156/Business_Insights_360/blob/main/Resources/Executive_view.png)

---

## Project Outcome

By using this report, decisions can be taken based on the data. Further it will help in answering n number of why questions based on the situations.


