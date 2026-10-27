# Lab 1: Data Visualization, Data Preprocessing, and Statistical Analysis

**Course:** MSCS-634-B01 — Advanced Big Data and Data Mining  
**Student:** Xhon Pelushi  
**University:** University of the Cumberlands

## Purpose

This lab applies data visualization, data preprocessing, and statistical analysis
techniques using Python in a Jupyter Notebook. A synthetic retail sales dataset
(400 transactions across five product categories) is explored, cleaned, and
statistically summarized.

## Key Insights

- **Visualizations:** Electronics transactions dominate in dollar value despite
  similar order volumes across categories. Customer ages are approximately
  normally distributed around the mid-thirties. Sales are spread fairly evenly
  across all five regions.
- **Preprocessing:** The IQR method identified 38 outlier transactions with
  unusually high total amounts. Missing values in UnitPrice, CustomerAge, and
  Rating were imputed using median and mean strategies. Min-Max scaling
  compressed numeric features into the [0, 1] range.
- **Statistical Analysis:** Quantity and UnitPrice are the strongest predictors
  of TotalAmount (correlations of 0.49 and 0.63 respectively). Customer age
  and rating show near-zero correlation with financial variables, indicating
  spending patterns are not strongly age-dependent.

## Challenges and Decisions

- **Missing value strategy:** UnitPrice was imputed per-category (median) rather
  than globally, because price distributions differ significantly between
  Electronics and Books.
- **Outlier threshold:** The standard 1.5 x IQR rule flagged 38 records as
  outliers. A more aggressive 3 x IQR threshold was considered but rejected to
  keep the demonstration clearer.
- **Data reduction:** OrderID was dropped as a non-analytical identifier. An 80%
  random sample was drawn to demonstrate sampling-based reduction while
  retaining distributional properties.

## Files

| File | Description |
|------|-------------|
| `Lab1_DataVisualization_Preprocessing_StatisticalAnalysis.ipynb` | Jupyter Notebook with all code, visualizations, and analysis |
| `retail_sales_data.csv` | Synthetic retail sales dataset (400 records, 10 attributes) |
| `README.md` | This file |
