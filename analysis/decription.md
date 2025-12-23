## 📊 Data Warehouse Analytics (Gold Layer)

This section focuses on **business-level analytics** performed on the **Gold layer** of the Data Warehouse.  
The goal was to transform curated data into **actionable insights and key performance indicators (KPIs)** for reporting and decision-making.

---

### 🔍 Exploratory & Descriptive Analysis

- Explored **customer geography**, **product categories**, and **sales timelines**
- Identified **first and last order dates** and calculated the overall sales duration
- Analyzed **customer demographics**, including age distribution and active customers
- Evaluated **product distribution** across categories and subcategories

---

### 📈 Sales & Revenue Analysis

- Calculated **total sales** and **total quantity sold**
- Computed **average selling price** and **average product cost** by category
- Measured **total revenue by category**, reported in millions
- Analyzed **sales performance by country** and ranked countries based on total revenue

---

### 👥 Customer Analytics

- Calculated **revenue generated per customer**
- Identified **top 10 highest-revenue customers**
- Determined the number of **customers who placed at least one order**
- Analyzed **quantity distribution by customer country**

---

### 🛒 Product Performance Analysis

- Identified **top 10 products by total sales**
- Determined the **best-selling product within each category**
- Used **window functions** to rank products by sales performance
- Analyzed product contribution to overall business revenue

---

### 📌 Key Techniques Used

- SQL Aggregations (`SUM`, `AVG`, `COUNT`)
- Window Functions (`ROW_NUMBER`, `RANK`)
- Common Table Expressions (CTEs)
- Joins across fact and dimension tables
- Business-friendly formatting for reporting metrics

---

### 🎯 Outcome

This analytics layer supports:
- Executive and operational **business reporting**
- **Dashboard development** (Power BI / Tableau)
- **Performance benchmarking** across products, customers, and regions
- Data-driven **strategic decision-making**

---

