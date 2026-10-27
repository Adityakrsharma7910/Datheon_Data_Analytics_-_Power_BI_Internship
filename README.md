# Business Analytics Portfolio: Financial Variance, Superstore Sales & Telco Churn

Three small analytics projects that turn raw business data into decisions, built for Power BI (DAX, star-schema modelling) with Python-based data cleaning and a standalone HTML dashboard.

| Project | Question it answers | Main outputs |
|---|---|---|
| [1. Financial Variance & Margin](#1-financial-variance--margin-dashboard) | Where does revenue erode between gross sales and profit, and what if costs or discounts change? | Interactive HTML dashboard, DAX measures |
| [2. Superstore Sales](#2-superstore-sales-analysis) | Which regions and products make or lose money? | Cleaned data, Power BI starter model, PDF report |
| [3. Telco Customer Churn](#3-telco-customer-churn) | Which customers are most likely to leave? | Cleaned data, high-risk segment table |

---

## 1. Financial Variance & Margin Dashboard

Models the income statement of the Microsoft Financial Sample (700 transactions, 2013-2014, 5 segments, 5 countries, 6 products):

**Gross Sales → Discounts → Net Sales → COGS → Profit**

**What it includes**
- Waterfall chart showing revenue erosion through discounts and COGS
- Actual vs budget variance by Segment, Country or Product
- Scenario sliders for unit volume, discount rate, manufacturing cost and budget growth
- DAX measures: `Gross Profit %`, `COGS Ratio`, `Discount Rate`, `Segment Margin`, variance and scenario measures

**Key findings**
- Margins are thin: gross profit is about 14-15% of net sales, and COGS takes about 85%.
- Discounts cost about 7% of gross sales, so cost changes move profit far more than discount changes.
- 58 of 700 rows (about 8%) are loss-making.

**Limitations**
- The source has no budget, so the budget is a placeholder (prior-year net sales × growth).
- 2013 is a partial year (175 rows vs 525 in 2014), which inflates year-over-year growth.
- There is no cost-center field, so COGS by product is used as a proxy.

**Files:** `Financial_Variance___Margin_Dashboard.html`, `financial_measures.dax`, `financial_sample.xlsx`

---

## 2. Superstore Sales Analysis

Cleaned Superstore order data (2015-2018) with a star-schema model ready for Power BI.

**Headline numbers:** $2.30M sales, $286K profit, 12.5% margin, 5,015 orders, 10,296 rows after duplicate removal.

**Insights**
- West leads on sales ($725K) and profit ($108K, 14.9% margin).
- Central has the weakest margin (7.9%) despite $501K in sales.
- Tables, Bookcases and Supplies lose money; Copiers, Phones and Accessories drive profit.
- Discounts should be judged against profit, not sales alone.

**Files**
- `superstore_sales_cleaned.csv`: cleaned data with `Year-Month`, `Month` and `Discount Band` columns
- `Superstore_PowerBI_Starter_Model.xlsx`: `Fact Orders`, `Dim Customer`, `Dim Product`, `Dim Date`, plus region and product summaries
- `Superstore_Executive_Sales_Report.pdf`: supporting report (not a Power BI export)

---

## 3. Telco Customer Churn

Cleaned telecom customer data (7,043 customers, 26.5% overall churn) with tenure cohorts, monthly charge bands and a churn flag.

**Highest-risk segments**

| Segment | Customers | Churned | Churn rate |
|---|---|---|---|
| Fiber optic + no tech support | 2,230 | 1,101 | 49.4% |
| First 12 months | 2,186 | 1,037 | 47.4% |
| Electronic check payers | 2,365 | 1,071 | 45.3% |
| Month-to-month contract | 3,875 | 1,655 | 42.7% |

All four segments churn well above the 26.5% average. Early tenure, no contract commitment and missing tech support are the strongest warning signs.

**Files:** `telco_churn_cleaned.csv`, `high_risk_segments.csv`

---

## How to use

1. Clone or download the repository.
2. **HTML dashboard:** open `Financial_Variance___Margin_Dashboard.html` in any browser.
3. **Power BI:** open Power BI Desktop, then *Get data → Excel/CSV* and load the files for the project you want.
4. **DAX measures:** open `financial_measures.dax` in Notepad or VS Code and paste each measure via *Table tools → New measure*. Name the loaded table `Financials` and rename the ` Sales` column to `Net Sales` first.

## Tech stack

Power BI Desktop · DAX · Power Query (M) · Python (pandas) · HTML/JavaScript · Excel

## Notes

- The `.dax` file and PDF are build guides and reports. No `.pbix` file is included.
- Datasets are public sample data (Microsoft Financial Sample, Superstore, Telco Customer Churn), used for learning and demonstration.
