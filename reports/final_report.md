# E-Commerce Sales Analysis Report
**Week 1 — Data Science Internship**

**Author:** Sankalp Padhi

## 1. Project Overview

The objective of this project is to analyze e-commerce sales data, validate data quality, calculate sales KPIs, identify business insights, and present findings through visualizations.

## 2. Tools Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## 3. Dataset Overview

- Original records: 100
- Original columns: 12
- Cleaned dataset columns: 13
- Additional calculated field: Total Amount

## 4. Data Quality Assessment

Initial checks found no missing values, fully duplicated rows, or repeated Order IDs.

Validation checks found no zero or negative quantities, zero or negative prices, negative ages, ratings outside the expected 1–5 range, or unparseable order dates.

Text fields were standardized, dates were converted into a consistent format, and Total Amount was calculated using Quantity × Price. No rows were removed.

## 5. Key Performance Indicators

| KPI | Result |
|---|---:|
| Total Revenue | ₹694,219.87 |
| Total Orders | 100 |
| Average Order Value | ₹6,942.20 |
| Total Units Sold | 294 |

## 6. Key Findings

- Electronics generated the highest category revenue at ₹140,811.26.
- Curtains were the top product by quantity sold, with 25 units.
- Curtains also generated ₹79,023.10 in product revenue.
- August 2024 recorded the highest monthly revenue at ₹94,121.76.
- Chennai recorded the highest order count, with 22 orders.
- The dataset contains 98 unique customers and 2 repeat customers.
- Repeat customers generated ₹17,107.31 in revenue.

## 7. Recommendations

1. Investigate the performance of Electronics and identify opportunities to improve its sales.
2. Review Curtains' pricing, availability, and promotion strategy because it leads in both units sold and product revenue.
3. Analyze monthly sales trends to understand peak and low-performing periods.
4. Explore customer retention campaigns to encourage repeat purchases.
5. Examine city-level performance to identify opportunities for localized marketing.

## 8. Deliverables

- Jupyter Notebook containing data cleaning and analysis.
- Cleaned CSV dataset.
- Revenue-by-category bar chart.
- Monthly sales trend line chart.
- Payment-method distribution pie chart.
- Dashboard mockup.

## 9. Conclusion

The project demonstrates a complete introductory sales-analysis workflow, from data inspection and validation to KPI calculation and visualization. The findings provide a starting point for further analysis of product performance, customer retention, and sales trends.

The results describe this 100-transaction dataset and should not automatically be generalized to a larger business population.
