# SALES DATA ANALYSIS

### Project Overview
---

This data analysis project aims to provide insights into the sales performance of a retail store. By analyzing various aspects of the sales data, We seek to identify trends, make data driven recommendations and gain deeper understanding of the Retail Store's performance.

![SALES DATA DASHBOARD REPORT](https://github.com/user-attachments/assets/a2f61d5b-2c1d-4a0a-8d7e-09bfd1712de2)

### Data Sources

Sales Data: The primary data set used for this analysis is the "Sales_data.csv file" containing detailed information about each sales made by the store.

### Tools Used

- Excel - Data cleaning, and analysis with pivot table
   - [Download here](https://microsoft.com)
- SQL - Data analysis
   - [Download here](https//microsoft.com)
- Power BI - Creating reports
   - [Download here](https//microsoft.com)
 
### Data Prepation

Initail data preparation phase, I performed the following tasks:

1. Data loading and inspection
2. Handling duplicates
3. Data cleaning

### Process

- Excel 
  - Data cleaning to ensure data is consistent with data format and values
  - Created pivot table according to questions asked
- SQL
  - Created tables to answer key questions
- Power BI
  - Created an interactive dashboard to generate more insights


### Exploratory Data Analysis

EDA involved exploring the sales data to answer key questions, such as;

- Find the highest selling products
- What is the monthly sale's trend for the current yaer
- Find the Regional performance for each prooduct

  
### Data Analysis

Some interesting code worked with;
~~~SQL
SELECT Product, sum(Sales) AS ProductSales
FROM  [dbo].[Sales_Data]
GROUP BY Product
ORDER BY 2 DESC

SELECT Region, Count(Sales) AS TransactionCount
FROM [dbo].[Sales_Data]
GROUP BY Region

SELECT TOP 1 Product, SUM(Sales) AS PopularProduct
FROM [dbo].[Sales_Data]
GROUP BY Product

SELECT OrderDate, sum(Sales) As Totalsales
from [dbo].[Sales_Data]
WHERE 
Year(OrderDate) = '2024'
GROUP BY OrderDate 
order by 2 DESC

SELECT Product FROM [dbo].[Sales_Data]
GROUP BY Product
HAVING MAX(OrderDate) < DATEADD(Quarter,-1,GETDATE())
~~~

### Results/Findings

- Shoes category is the best performing category in terms of sales and revenue
- The store's highest revenue is generated from customers with High-LIV
- Retail store's sales have been unsteady, with a peak in the month of February and August
- South, being most of the customers' location, is the overall performing region in terms of sales and revenue, generating 44% of the store's revenue

### Recommendations

Based on analysis, I recommend the following actions;
- Focus on expanding and promoting the shoes category
- Implement a customer segmentation strategy to target high-LIV customers effectively
- Invest in marketing and promotions during peak sales period to maximize revenue
- The south region should be targeted for more marketing strategies









