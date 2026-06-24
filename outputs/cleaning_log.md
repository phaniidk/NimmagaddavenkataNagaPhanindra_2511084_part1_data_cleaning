# Cleaning Log

## Issues Found

1. Extra spaces in text fields
2. Case inconsistencies in categorical columns
3. Mixed date formats
4. Missing values in Region, Ship Mode, and Discount
5. Duplicate records
6. Invalid discount values
7. Invalid shipping records (ship date before order date)
8. Sales-profit mismatches
9. Invalid order status values
10. Invalid payment status values

## Cleaning Actions Performed

- Removed leading and trailing spaces using TRIM()
- Standardized text case using PROPER()
- Standardized date formats
- Replaced missing Region values with "Unknown"
- Replaced missing Ship Mode values with "Unknown"
- Replaced missing Discount values with 0
- Removed duplicate records
- Created calculated columns
- Applied validation checks

## Business Rules Applied

- Missing Region → Unknown
- Missing Ship Mode → Unknown
- Missing Discount → 0
- Cancelled orders excluded from completed sales analysis
- Failed payments excluded from completed sales analysis
- Refunded orders analyzed separately

## Validation Results

| Issue | Count |
|---------|--------:|
| Invalid Discounts | 41 |
| Invalid Shipping Records | 148 |
| Sales Validation Errors | 40 |
| Invalid Order Status Values | 163 |
| Invalid Payment Status Values | 71 |

## Assumptions Made

- Cost field represents total order cost.
- Missing Region and Ship Mode values were replaced with Unknown as per business rules.
- Missing Discount values were treated as 0.
- Validation errors were flagged instead of deleting records.

## Final Dataset Summary

- Original Records: 932
- Duplicate Rows Removed: 14
- Final Records: 912
