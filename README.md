#  Customers Order Tracker (Using Power BI)

##  Problem Statement:

Businesses often struggle to track revenue performance, understand customer behavior, and identify factors leading to order cancellations or pending transactions. Without clear insights, it’s difficult to make informed decisions on sales strategies, customer retention, and marketing optimization.

## Data Cleaning Process
1. Customer Table (10 columns, 3000 rows)

Removed Duplicates: Dropped duplicate records based on customer_id and name. After cleaning, rows reduced from 3000 → 50 → 33.

Email Column: Replaced blank/empty values with unknown@example.com.

Age Column: Converted data type to whole number.

Gender Column: Standardized entries to only Male and Female.

Date Column:

Identified 2 invalid dates and wrong data type.

Duplicated the column and reformatted using English (United States) locale.

Replaced invalid values with null and applied fill down to correct gaps.

2. Order Table

Found 1 customer (C099) with 151 orders whose ID did not exist in the Customer table (highlighting a data integrity issue).

Order Status Column: Standardized inconsistent spellings — e.g., completed, Completed, Complete → Completed.

Release Date Column: Corrected invalid date formats using the same locale method.

3. Product Table

Removed duplicate entries based on product_name.

4. Review Table

Removed duplicate rows based on review_id to ensure each review is unique.

5. Transaction Table

Performed a left join between Customers and Orders to ensure all customer records were retained.

Joined remaining customer-related tables to track only customers with at least one order history (removing orphan records with no transactions).

 Final dataset is clean, consistent, and relationally accurate, enabling reliable insights on customer behavior, product performance, and transaction tracking.
