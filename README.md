# SQL_Project_Sales_data

This Project Involves analyzing a sample sales dataset using sql server(ssms). The goal is extract business insights such as total_sales, Top Products, and region wise performamce using SQL queries. 

##  Dataset Description


The dataset contains sample sales data with the following columns:

| Column Name    | Description                          |
|----------------|--------------------------------------|
| OrderID        | Unique ID for each order             |
| CustomerName   | Name of the customer                 |
| Product        | Name of the product sold             |
| Category       | Product category (Electronics, etc.) |
| Quantity       | Number of units sold                 |
| Price          | Price per unit                       |
| OrderDate      | Date of the order                    |
| Region         | Sales region (North, South, etc.)    |



##  Tools Used

- SQL Server Management Studio (SSMS)
- T-SQL (Transact-SQL)

  
##  Objectives

- Load and explore sales data
- Calculate total revenue
- Identify top-selling products
- Analyze region-wise performance

  
##  SQL Queries Used

 1. View all data

```sql
SELECT * FROM SalesData;


 2. Calculate Total Sales
sql

SELECT SUM(Quantity * Price) AS TotalSales FROM SalesData;
Calculates total sales revenue.

3. Region-wise Sales

SELECT Region, SUM(Quantity * Price) AS SalesByRegion
FROM SalesData
GROUP BY Region;
Displays total sales for each region.

4. Top 5 Most Sold Products

SELECT Product, SUM(Quantity) AS TotalQty
FROM SalesData
GROUP BY Product
ORDER BY TotalQty DESC
OFFSET 0 ROWS FETCH NEXT 5 ROWS ONLY;
 Lists the 5 products with highest quantity sold.

##  Key Insights
Most revenue comes from Electronics category.

West and North regions show high sales.

Top-selling products include Laptop, Mobile, and Headphones.

##  Conclusion
This project demonstrates how SQL can be used effectively to analyze business sales data, extract trends, and support data-driven decision-making.


