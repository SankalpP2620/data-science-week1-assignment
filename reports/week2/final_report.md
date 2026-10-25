
# E-Commerce Sales Analysis and Prediction — Week 2

**Author:** Sankalp Padhi  
**Program:** WelIntern Data Science  
**Week:** 2

## 1. Project Overview

This project focuses on data cleaning, exploratory data analysis (EDA), business insights, and sales prediction using Python. The dataset is a synthetic e-commerce sales dataset containing intentional data-quality issues for learning purposes.

The objective is to prepare the data, identify sales patterns, compare machine learning models, and evaluate their predictive performance.

## 2. Tools and Technologies

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Jupyter Notebook

## 3. Dataset and Data Cleaning

The raw dataset is stored at `data/raw/week2_raw_ecommerce_sales.csv`. The original raw dataset was preserved, and processed data was saved separately.

The cleaning and preprocessing workflow included:

- Removing exact duplicate rows.
- Standardizing category spellings and common text formatting.
- Parsing numeric fields with mixed representations.
- Treating implausible quantity, price, age, and rating values as missing before imputation.
- Filling missing numeric values using medians and categorical values using modes.
- Removing records with missing or invalid order dates when dates could not be reliably inferred.
- Applying outlier thresholds based on business assumptions.

Duplicate Order IDs were reduced to one row per ID. In a real business dataset, repeated IDs should be investigated before removal because they may represent legitimate line items.

## 4. Exploratory Data Analysis

The notebook generated visualizations to explore the dataset and its relationships, including:

1. Order amount distribution.
2. Correlation heatmap.
3. Revenue by category.
4. Monthly sales trend.
5. Sales amount by delivery status.
6. Quantity versus amount.
7. Actual versus predicted sales.

These charts support the exploration of sales distributions, category performance, time-based trends, delivery outcomes, and relationships between order quantities and sales amounts.

## 5. Sales Prediction Models

Two regression models were evaluated to predict `total_amount` using quantity, unit price, category, city, and payment mode:

- Linear Regression
- Random Forest Regressor

The dataset was split into training and testing sets using an 80:20 split with `random_state=42`. Both models were evaluated using Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R-squared (R²).

### Model Comparison

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Random Forest | 648.15 | 934.75 | 0.9292 |
| Linear Regression | 1967.05 | 2491.44 | 0.4972 |

Random Forest performed better on the test set, with lower MAE and RMSE and a higher R² score.

The Random Forest model was therefore selected as the best-performing model among the two evaluated models.

## 6. Data Quality and Limitations

The analysis involved several cleaning decisions that require business-context validation, especially duplicate Order ID handling and outlier thresholds.

The results have important limitations:

- The dataset is small and synthetic.
- The evaluation uses a random train/test split.
- Historical features are limited.
- The model metrics are educational results and should not be interpreted as evidence of production forecasting performance.

The model may perform differently on larger, real-world datasets.

## 7. Key Findings

- Random Forest outperformed Linear Regression on the test set.
- The Random Forest model achieved an RMSE of approximately 934.75 and an R² score of approximately 0.9292.
- Data cleaning and consistent preprocessing were important parts of the workflow.
- The actual-versus-predicted plot was used to visually inspect prediction performance.

## 8. Recommendations

1. Validate cleaning rules with a domain expert before applying them to real business data.
2. Collect a larger and more representative dataset.
3. Add useful historical sales features where available.
4. Evaluate models using cross-validation and additional test data.
5. Monitor model performance before using predictions for business decisions.

## 9. Deliverables

- Jupyter Notebook: `notebooks/week2_data_science_assignment.ipynb`
- Raw dataset: `data/raw/week2_raw_ecommerce_sales.csv`
- Cleaned dataset: `data/cleaned/`
- Visualizations: `outputs/week2_charts/`
- KPI summary: `reports/week2/week2_kpi_summary.csv`
- Model comparison: `reports/week2/week2_model_comparison.csv`
- Data-quality comparison: `reports/week2/week2_quality_comparison.csv`

## 10. Conclusion

This project demonstrates an end-to-end introductory data science workflow, from data cleaning and exploratory analysis to regression model comparison.

Random Forest achieved better test-set performance than Linear Regression on this dataset. However, because the data is small and synthetic, further validation is required before applying the approach to real-world sales forecasting.
