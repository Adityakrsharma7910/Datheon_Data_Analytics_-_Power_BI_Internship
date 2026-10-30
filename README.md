# Data Analytics & Power BI Internship

A collection of business analytics projects focused on financial performance, sales and profitability analysis, and customer churn analysis. This repository demonstrates practical data analytics workflows using cleaned datasets, business KPIs, DAX measures, data modeling, and interactive reporting.

## 📌 Project Overview

This repository contains three analytics projects designed to transform business data into meaningful insights and support data-driven decision-making.

| Project | Business Objective | Key Deliverables |
|---|---|---|
| Financial Variance & Margin Dashboard | Understand revenue, costs, profit margins, and budget variance | Interactive HTML dashboard and DAX measures |
| Superstore Sales Analysis | Analyze sales, profitability, regional performance, and discounts | Cleaned CSV, Power BI starter model, and executive PDF report |
| Telco Customer Churn Analysis | Identify customer groups with high churn rates | Cleaned customer dataset and high-risk segment analysis |

## 🛠️ Tech Stack

- **Power BI:** Dashboard development and business intelligence
- **DAX:** KPI calculations, financial measures, and year-over-year analysis
- **Power Query (M):** Data transformation concepts
- **Python (Pandas):** Data cleaning and analytical preparation
- **SQL:** Data analysis and querying concepts
- **Excel:** Dataset preparation and data modeling
- **HTML, CSS & JavaScript:** Interactive financial dashboard

## 📊 Project 1: Financial Variance & Margin Dashboard

### Objective
Analyze financial performance by understanding how gross sales are affected by discounts and costs before generating profit. Explore how changes in sales volume, discount rates, and manufacturing costs can influence profitability.

### Key Features
- Financial performance analysis: Gross Sales → Discounts → Net Sales → COGS → Profit.
- Revenue erosion waterfall visualization.
- Actual-versus-budget comparison by segment, country, and product.
- Interactive scenario controls for sales volume, discount rate, manufacturing cost, and budget growth.
- Financial KPIs including profit margin, cost-of-goods-sold ratio, discount rate, and variance percentage.

### Key Insights
- Gross profit margin is approximately 14–15% of net sales in the analyzed sample.
- Cost of Goods Sold (COGS) accounts for approximately 85% of net sales.
- 58 of 700 records are loss-making, representing approximately 8.3% of the dataset.
- Cost changes can significantly affect profitability, making margin analysis important alongside revenue growth.

### Business Value
The dashboard helps users understand where revenue is reduced, compare financial performance across business dimensions, and evaluate hypothetical business scenarios before making decisions.

**Files:**
- [Financial Variance & Margin Dashboard](./Financial%20Variance%20%26%20Margin%20Dashboard.html)
- [Financial DAX Measures](./financial_measures.dax)

**Important limitation:** The original financial sample does not contain actual budget values. Budget comparisons use an illustrative budget derived from prior-year actual sales and an assumed growth rate. Scenario outputs are simulations, not forecasts.

## 📈 Project 2: Superstore Sales Analysis

### Objective
Analyze retail sales and profitability to identify high-performing regions, profitable product categories, and potential losses associated with discounting.

### Key Analysis
- Total sales, profit, order count, and profit margin.
- Regional sales and profitability comparison.
- Category and sub-category performance.
- Monthly sales trends and year-over-year comparisons.
- Discount sensitivity and loss-making products.
- Executive-level KPIs and Power BI data-model preparation.

### Key Findings
Based on the current repository's documented analysis:

- Total sales are approximately **$2.30 million**.
- Total profit is approximately **$286,000**.
- Overall profit margin is approximately **12.5%**.
- The West region leads in sales and profit, with approximately $725,000 in sales and $108,000 in profit.
- The Central region has a comparatively low profit margin of approximately 7.9%.
- Tables, Bookcases, and Supplies are identified as loss-making product groups in the documented analysis.
- Discounts should be evaluated against their effect on profit rather than sales alone.

### Power BI Data Model
The starter workbook includes a star-schema-style structure with:

- **Fact Orders:** Transaction-level sales, quantity, discount, and profit data.
- **Dim Customer:** Customer and regional attributes.
- **Dim Product:** Product category and sub-category attributes.
- **Dim Date:** Date-related fields for time-based analysis.

### Key DAX Measures
The accompanying model guide provides measures and guidance for:

- Total Sales
- Total Profit
- Total Orders
- Total Quantity
- Profit Margin %
- Sales Previous Year
- Year-over-Year Sales Growth %
- Average Discount

**Files:**
- [Cleaned Superstore Sales Dataset](./superstore_sales_cleaned.csv)
- [Power BI Starter Model](./Superstore_PowerBI_Starter_Model.xlsx)
- [Superstore DAX & Model Guide](./Superstore_DAX_and_Model_Guide.txt)
- [Superstore Executive Sales Report](./Superstore_Executive_Sales_Report.pdf)

**Business Value:** This analysis supports regional performance evaluation, product-level profitability analysis, and better discounting decisions.

## 📉 Project 3: Telco Customer Churn Analysis

### Objective
Analyze customer churn patterns to identify customer groups that may require retention-focused business strategies.

### Dataset Overview
- Approximately 7,043 customer records.
- Customer demographics and service information.
- Tenure, contract type, payment method, and monthly charges.
- Churn status and a numeric churn flag.
- Additional tenure cohorts and monthly charge bands for segmentation.

### Key Findings
The documented analysis reports an overall churn rate of approximately **26.5%**.

| High-Risk Customer Segment | Customers | Churned Customers | Churn Rate |
|---|---:|---:|---:|
| Fiber optic with no tech support | 2,230 | 1,101 | 49.4% |
| First 12 months of tenure | 2,186 | 1,037 | 47.4% |
| Electronic check payers | 2,365 | 1,071 | 45.3% |
| Month-to-month contracts | 3,875 | 1,655 | 42.7% |

### Business Recommendations
- Focus retention efforts on customers in their first year.
- Evaluate additional technical support options for fiber-optic customers.
- Investigate churn patterns among electronic check payers.
- Encourage longer-term contracts where appropriate.
- Monitor churn rates across customer tenure and payment segments.

These segments show higher churn rates than the reported overall average. They identify areas for further investigation, rather than proving that any single factor causes churn.

**Files:**
- [Cleaned Telco Customer Dataset](./telco_churn_cleaned.csv)
- [High-Risk Customer Segments](./high_risk_segments.csv)

## 📁 Repository Structure

```text
Datheon_Data_Analytics_-_Power_BI_Internship/

│
├── Financial Variance & Margin Dashboard.html
├── financial_measures.dax
│
├── superstore_sales_cleaned.csv
├── Superstore_PowerBI_Starter_Model.xlsx
├── Superstore_DAX_and_Model_Guide.txt
├── Superstore_Executive_Sales_Report.pdf
│
├── telco_churn_cleaned.csv
└── high_risk_segments.csv
```

## 🚀 How to Use This Repository

1. Clone or download the repository.
2. Open the financial dashboard HTML file in a modern web browser to explore its interactive controls.
3. Open the Superstore CSV or Excel workbook to inspect the prepared dataset and data model.
4. Open Power BI Desktop and import the relevant CSV or Excel file using **Home → Get Data**.
5. Follow the DAX and model guide to create relationships, measures, KPI cards, charts, and slicers.
6. Open the executive sales report PDF to review the documented Superstore analysis.
7. Use the cleaned Telco dataset and high-risk segment CSV to explore customer churn patterns.

## 📚 Skills Demonstrated

- Data cleaning and preparation
- Exploratory data analysis
- KPI development and financial analysis
- DAX measures and time-based analysis
- Star-schema data modeling concepts
- Sales and profit-margin analysis
- Customer segmentation and churn analysis
- Interactive dashboard design
- Business insights and recommendations
- GitHub project documentation

## ⚠️ Data & Project Notes

- The projects use sample datasets for learning and demonstration.
- The financial dashboard uses an illustrative budget assumption because actual budget figures are not available in the source data.
- The financial HTML dashboard is a standalone interactive deliverable; it is not a Power BI `.pbix` file.
- The Superstore PDF is a supporting executive report, not an exported Power BI dashboard.
- The repository contains a Power BI starter model and DAX guidance, but a finished `.pbix` file is not currently included.
- Reported metrics and findings are based on the documented analysis and should be revalidated if the underlying data or transformation logic changes.

## 🎯 Conclusion

These projects demonstrate how business data can be prepared, analyzed, and presented to answer practical questions about financial performance, retail profitability, and customer retention.

The overall objective is to convert raw or prepared datasets into useful business insights through data analysis, business intelligence techniques, and clear reporting.

---

**Project:** Datheon Data Analytics & Power BI Internship  
**GitHub Repository:** [View Project Repository](https://github.com/Adityakrsharma7910/Datheon_Data_Analytics_-_Power_BI_Internship)


