# Customer Retention & Churn Analysis

## Project Overview

Customer retention is one of the most important factors influencing the growth and profitability of subscription-based businesses. This project analyzes customer churn patterns and identifies key factors that affect customer retention.

The analysis provides business insights and recommendations to help improve customer loyalty and reduce churn.

---
## Objectives

- Analyze customer churn patterns.
- Identify customer segments with high churn rates.
- Understand customer lifetime trends.
- Evaluate retention drivers.
- Provide actionable recommendations to improve customer retention.

---

## Tools Used

- Microsoft Power BI
- Power Query Editor
- DAX Measures
- Data Visualization

---

## Dataset

### Telco Customer Churn Dataset

The dataset contains information about:

- Customer ID
- Gender
- Contract Type
- Internet Service
- Payment Method
- Monthly Charges
- Customer Tenure
- Churn Status

**Total Customers:** 7,043

---

## DAX Measures Created

### Total Customers

```DAX
Total Customers =
COUNT('WA_Fn-UseC_-Telco-Customer-Churn'[customerID])
```

### Churned Customers

```DAX
Churned Customers =
CALCULATE(
COUNT('WA_Fn-UseC_-Telco-Customer-Churn'[customerID]),
'WA_Fn-UseC_-Telco-Customer-Churn'[Churn] = "Yes"
)
```

### Retained Customers

```DAX
Retained Customers =
CALCULATE(
COUNT('WA_Fn-UseC_-Telco-Customer-Churn'[customerID]),
'WA_Fn-UseC_-Telco-Customer-Churn'[Churn] = "No"
)
```

### Churn Rate %

```DAX
Churn Rate % =
DIVIDE([Churned Customers],[Total Customers])
```

### Retention Rate %

```DAX
Retention Rate % =
DIVIDE([Retained Customers],[Total Customers])
```

### Average Monthly Charges

```DAX
Average Monthly Charges =
AVERAGE('WA_Fn-UseC_-Telco-Customer-Churn'[MonthlyCharges])
```

### Average Tenure

```DAX
Average Tenure =
AVERAGE('WA_Fn-UseC_-Telco-Customer-Churn'[tenure])
```

---

## Dashboard Pages

### Page 1: Customer Churn Analysis

#### KPI Metrics

- Total Customers
- Churned Customers
- Retained Customers
- Churn Rate %
- Retention Rate %
- Average Monthly Charges
- Average Tenure

#### Visualizations

- Customer Churn Distribution
- Contract Type vs Churn
- Internet Service vs Churn
- Payment Method vs Churn
- Gender vs Churn
- Interactive Slicers

---

### Page 2: Retention & Lifetime Analysis

#### Visualizations

- Retained Customers by Contract
- Retained Customers by Internet Service
- Retained Customers by Payment Method
- Average Tenure by Contract

#### KPI Cards

- Average Monthly Charges
- Average Tenure
- Retention Rate %

---

### Page 3: Customer Insights & Recommendations

#### Treemap

- Customer Distribution by Internet Service

#### Key Insights

- Two-year contract customers exhibit the highest retention.
- Fiber optic customers show relatively higher churn.
- Customers with longer tenure are less likely to leave.
- Electronic check users display higher churn behavior.

---

## Key Findings

- Approximately **26.5%** of customers have churned.
- Around **73.5%** of customers are retained.
- Long-term contracts significantly improve retention.
- Customer tenure has a strong impact on loyalty.
- Payment methods influence customer churn behavior.

---

## Recommendations

- Promote long-term contracts.
- Improve customer experience for fiber optic users.
- Encourage automatic payment methods.
- Reward loyal customers with retention programs.
- Focus on high-risk customer segments.

---

## Conclusion

This project demonstrates how Power BI can be used to analyze customer churn and retention patterns. The insights generated from this analysis can help businesses improve customer loyalty and achieve sustainable growth.
