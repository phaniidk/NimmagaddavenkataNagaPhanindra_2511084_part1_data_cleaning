# NimmagaddavenkataNagaPhanindra_2511084_part1_data_cleaning

# Business Data Cleaning, Validation & Excel Reporting

## Project Summary

This project focuses on cleaning, validating, and analyzing retail sales data. The objective was to improve data quality, apply business rules, identify issues, and generate Excel-based reports for management review.

---

## Dataset Description

The dataset contains order-level sales information including:

- Order ID
- Customer Details
- Region
- Category
- Sub Category
- Sales
- Cost
- Profit
- Discount
- Payment Status
- Order Status
- Order Date
- Ship Date

---

## Data Cleaning Performed

### Text Cleaning

- Removed extra spaces
- Standardized capitalization
- Fixed inconsistent category names

### Date Cleaning

- Standardized date formats
- Validated order and ship dates

### Missing Values

| Column | Action |
|----------|----------|
| Region | Replaced with Unknown |
| Ship Mode | Replaced with Unknown |
| Discount | Replaced with 0 |

### Duplicate Handling

- Removed 14 exact duplicate records

---

## Business Rules Applied

- Missing Region → Unknown
- Missing Ship Mode → Unknown
- Missing Discount → 0
- Cancelled orders excluded from completed sales analysis
- Failed payments excluded from completed sales analysis
- Refunded orders reported separately

---

## Data Quality Issues Found

| Issue | Count |
|---------|--------:|
| Invalid Discounts | 41 |
| Invalid Shipping Records | 148 |
| Sales Validation Errors | 40 |
| Invalid Order Status Values | 163 |
| Invalid Payment Status Values | 71 |

---

## Reports Created

### Data Quality Report

Contains:

- Missing Values Summary
- Duplicate Summary
- Discount Validation
- Date Validation
- Order Status Summary
- Sales Validation
- Final Quality Summary

### Pivot Summary Report

Contains:

- Sales & Profit by Region
- Sales & Profit by Category
- Orders by Ship Mode
- Profit Margin by Segment
- Refunded Orders by Region
- Monthly Sales Trend

---

## Key Business Insights

- 14 duplicate records were removed.
- 148 shipping records had invalid shipping dates.
- 41 records contained invalid discount values.
- 163 records had invalid order status values.
- 71 records had invalid payment status values.
- Data quality improvements increased consistency and reporting accuracy.

---

## Assumptions & Limitations

- Cost values were treated as total order costs.
- Invalid records were flagged rather than deleted.
- Business rules were applied as specified in the assignment.
