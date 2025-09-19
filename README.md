<img width="32766" height="81" alt="image" src="https://github.com/user-attachments/assets/e0a64053-5f5e-42eb-8470-d625c5314156" /># Mobile_Sales_Analysis

## Overview:

**This is a sales report that examines sales patterns across different time periods, product categories, and customer segments to identify key growth opportunities and market dynamics**

---

## Contents
Project Overview | Data Source | Tools Used | Table Array | Query Language (SQL) | Visualization

---
## Project Overview:
> >This project analyzes the sales of Mobile Sales Products to uncover insights on sales distribution by various attributes such as Brands, Payment Method, Customer Gender and lot more using Pivot tables, I explored metrics like total sales by Payment Method and Gender, average income of buyers, gender distribution and overall revenue. This analysis helps to understand the key factors drivig sales in the dataset provided. 

## Data Source:
www.kaggle.com/dataset

## Tools Used:
+ Pivot Tables / Charts
+ PowerBI
+ SQL

  ## Table Outlay
  First three Records

 |TransactionID|	Date |MobileModel |Brand	|Price	|UnitsSold|	TotalRevenue	|CustomerAge|	CustomerGender|	Location |PaymentMethod|
 |-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
|79397f68-61ed-4ea8-bcb2-f918d4e6c05b|	1/6/2024	|direction	|Green Inc	|1196.95	|85	|28002.8	|32	|Female	|Port Erik	|Online|
|4f87d114-f522-4ead-93e3-f336402df6aa|	4/5/2024	|right	|Thomas-Thompson	|1010.34	|64	|2378.82	|55	|Female	|East Linda	|Credit Card|
|6750b7d6-dcc5-48c5-a76a-b6fc9d540fe1|	2/13/2024	|summer	| Sanchez-Williams	|400.8	|95	|31322.56	|57	|Male| East Angelicastad	|Online|

## Query Language: (SQL)
Some of the query language to retrieve records are displayed here

```SQL
---to categorize the data into silver, gold and diamond---
SELECT Price,
CASE
WHEN price <= 100 THEN 'Silver' WHEN Price >= 500 THEN 'Gold'
ELSE 'Diamond'
END
FROM [dbo].[mobile_sales];

```
```SQL
---to retrieve the sales by payment method arranging from largest to smallest amount---
SELECT PaymentMethod,SUM(TotalRevenue) AS Sales
  FROM [dbo].[mobile_sales]
  GROUP BY PaymentMethod
  ORDER BY Sales DESC;

```

## Visualization
### Pivot Tables

 <img width="889" height="429" alt="Mobile sales pivot table" src="https://github.com/user-attachments/assets/832f674d-c4c0-472a-92b7-e017107fb03a" />

 ### Charts
 
<img width="1021" height="402" alt="Mobile sales dashboard" src="https://github.com/user-attachments/assets/9e27e1a4-e5af-4081-b228-598f61121268" />
