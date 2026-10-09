# Customer Churn Dataset — Data Quality Audit

## Objective
Audit and clean a customer churn dataset, document quality decisions, and identify initial patterns.

## Dataset
- 15 customer records
- 11 columns
- Target: `Churn`

## Data-quality findings
- Missing values: **0**
- Duplicate rows: **0**
- IQR outliers in numerical columns: **0**
- `TotalCharges` mismatches against `MonthlyCharges × TenureMonths`: **0**
- All CustomerIDs are unique.

## Cleaning decisions
No values or rows were removed because the audit found no demonstrated data-quality problem requiring removal or imputation.

`TotalCharges` was validated against `MonthlyCharges × TenureMonths` and all records matched to two decimal places.

This follows a conservative principle: do not alter valid observations without evidence.

## Initial patterns
- Overall churn rate: **46.7%**
- Average tenure: **7.0 months for churned customers vs 29.1 months for retained customers**
- Average support tickets: **4.29 for churned customers vs 1.00 for retained customers**
- Month-to-month contract churn: **100%** in this sample
- Basic subscription churn: **71.4%** in this sample

## Important limitation
The dataset contains only 15 customers. These are descriptive patterns for exploration, not statistically reliable population-level conclusions.

## Files
- `customer_churn_audit.ipynb` — complete audit, cleaning decisions, validation, summaries, and charts
- `data/customer_churn_raw.csv` — original dataset
- `data/customer_churn_cleaned.csv` — validated cleaned dataset
