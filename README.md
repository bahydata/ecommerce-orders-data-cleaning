## Project: Data Cleaning - [data.csv]

### Problem
The dataset contained:
- Missing values in shipment_date (80 rows)
- Missing values in customer_email (22 rows)
- Missing values in delivery_city (13 rows)
- Inconsistent date formats in order_date, shipment_date and unit_price
- Inconsistent categorical values (e.g., "Credit Card", "credit card", "CREDIT CARD")
- Dulicated rows
- Logical inconsistencies:
  - shipment_date earlier than order_date (violates shipment_date >= order_date)
  - Missing shipment_date for Delivered/Shipped orders
---

### Solution
Applied data cleaning using Pandas:

### Solution
Applied data cleaning using Pandas:

- Removed duplicate rows
- Standardized date formats (order_date, shipment_date)
- Converted unit_price to numeric and handled parsing errors
- Normalized categorical values (e.g., payment_method)
- Validated logical rules:
  - Removed/flagged rows where shipment_date < order_date
  - Ensured shipment_date exists for Delivered and Shipped orders
- Handled missing values:
  - Kept customer_email and delivery_city as NaN (no reliable imputation)
  - Kept shipment_date as NaT for non-shipped orders
---

## Before vs After

### Before
- 320 rows with 4 duplicate records
- 89 invalid date relationships (shipment_date < order_date)
- 80 missing shipment_date, 22 missing customer_email, 13 missing delivery_city

### After
- Clean dataset with 222 rows and 0 duplicates
- All date relationships valid (0 logical errors)
- All missing values resolved (0 nulls in critical fields)
---

### Tools
- Python
- Pandas

---

### Deliverables
- Cleaned CSV
- Jupyter Notebook
- Cleaning Report

---

### Result
Dataset is now cleaned, standardized, and fully validated, ready for analysis