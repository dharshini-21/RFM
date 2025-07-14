SQL RFM Customer Segmentation Project

Objective:
---------
This project performs an RFM (Recency, Frequency, Monetary) segmentation analysis on customers using Google BigQuery's `thelook_ecommerce` dataset. The goal is to classify customers based on their purchase behavior and provide insights that help businesses understand their customer base better.

Segment customers into different categories such as:
----------------------------------------------------
Best Customers
High Spending New Customers
Lowest-Spending Active Loyal Customers
Churned Best Customers 
Based on their purchase data.

This helps in targeted marketing, customer retention, and optimizing business strategies.

SOURCE:
------
Google BigQuery Public Dataset(https://console.cloud.google.com/marketplace/product/bigquery-public-data/thelook-ecommerce)
Tables Used: 
  - `order_items`
  - `users`

Tools Used:
-----------
 - SQL 
 - Google BigQuery
 - GitHub

Steps:
------
1. Open Google BigQuery.
2. Copy the code from `RFM_Segmentation.sql`.
3. Run the script step-by-step.
4. Explore customer segments in the final output.


Recency	                                     Frequency	                                 Monetary
R-Tier-1 (most recent)          	F-Tier-1 (most frequent)	           M-Tier-1 (highest spend)
R-Tier-2	                        F-Tier-2	                           M-Tier-2
R-Tier-3	                        F-Tier-3	                           M-Tier-3
R-Tier-4 (least recent)	                F-Tier-4 (only one transaction)	           M-Tier-4 (lowest spend)


Customers are segregated based on the above RFM Tiers
●Best Customers – This group consists of those customers who are found in R-Tier-1, F-Tier-1 and M-Tier-1, meaning that they transacted recently, do so often and spend more than other customers. A shorthand notation for this segment is 1-1-1; we’ll use this notation going forward.

●High-spending New Customers – This group consists of those customers in 1-4-1 and 1-4-2. These are customers who transacted only once, but very recently and they spent a lot.

●Lowest-Spending Active Loyal Customers – This group consists of those customers in segments 1-1-3 and 1-1-4 (they transacted recently and do so often, but spend the least).

●Churned Best Customers – This segment consists of those customers in groups 4-1-1, 4-1-2, 4-2-1 and 4-2-2 (they transacted frequently and spent a lot, but it’s been a long time since they’ve transacted).



