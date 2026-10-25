# 📊 Business Insights 360 – Executive & Operational Analytics

[![Power BI](https://img.shields.io/badge/Power_BI-Desktop_%26_Service-F2C94C?logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![SQL](https://img.shields.io/badge/Database-MySQL-4479A1?logo=mysql&logoColor=white)](https://www.mysql.com/)
[![Git LFS](https://img.shields.io/badge/Git-LFS_Enabled-F05032?logo=git&logoColor=white)](https://git-lfs.github.com/)

---

## 🔗 Quick Links
* 🚀 **[Live Interactive Dashboard]([#](https://app.powerbi.com/view?r=eyJrIjoiNDgzYjBkNDctOTI0Zi00NTM1LWEwODQtYTA3ZmFjMzE0NWVkIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9))** 
* 📂 **[Data Model Architecture](#-data-architecture--modeling)**

---

## 📌 Project Overview & Context

**AtliQ Hardware** is a fast-growing global manufacturer selling computers and accessories through three primary channels: **Retailers**, **Direct**, and **Distributors** across physical store (*Brick & Mortar*) and *E-Commerce* platforms.

After experiencing unexpected market losses due to expanding into new territories based on static intuition and spreadsheet analysis, AtliQ leadership initiated **Business Insights 360**. This Power BI solution transitions the business from intuition-based decision-making to an automated, data-driven analytics culture across **Finance, Sales, Marketing, and Supply Chain**.

---

## 🛠️ Tech Stack & Tools

* **Business Intelligence:** Power BI Desktop, Power BI Service (Workspaces, Apps, Gateways)
* **Database & Querying:** MySQL Workbench (Relational Database Import)
* **Analytics & Calculations:** DAX (Data Analysis Expressions), M Language (Custom Date Tables)
* **Optimization & Data Engineering:** DAX Studio, Git LFS (Large File Storage tracking)
* **Project Management:** Project Charter, Stakeholder Alignment Framework

---

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

## 🗄️ Data Architecture & Modeling

The project integrates data from two MySQL databases (`gdb041` and `gdb056`) organized into a high-performance **Snowflake Schema** to balance normalization and analytical speed.
