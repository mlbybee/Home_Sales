# Module 22 - SparkSQL Challenge

## Overview:

Use your knowledge of SparkSQL to determine key metrics about home sales data. Then you'll use Spark to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

## Instructions:

1) Rename the Home_Sales_starter_code.ipynb file as Home_Sales.ipynb.
2) Import the necessary PySpark SQL functions for this assignment.
3) Read the home_sales_revised.csv from the provided AWS S3 bucket location into a PySpark DataFrame.
4) Create a temporary table called home_sales.
5) Answer the following questions using SparkSQL:
*  What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.

![Q1]()

*  What is the average price of a home for each year the home was built, that has three bedrooms and three bathrooms? Round off your answer to two decimal places.

![Q2]()

* What is the average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.

![Q3]()

* What is the average price of a home per "view" rating having an average home price greater than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.

![Q4]()

6) Cache your temporary table home_sales.
7) Check if your temporary table is cached.
8) Using the cached data, run the last query that calculates the average price of a home per "view" rating having an average home price greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.
* Cached Runtime
![Q4_cached]()

9) Partition by the "date_built" field on the formatted parquet home sales data.
10) Create a temporary table for the parquet data.
11) Run the last query that calculates the average price of a home per "view" rating having an average home price greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.
* Parquet Runtime
![Q4_parquet]()

12) Uncache the home_sales temporary table.
13) Verify that the home_sales temporary table is uncached using PySpark.
14) Download your Home_Sales.ipynb file and upload it into your "Home_Sales" GitHub repository.

## Results:

## Summary:

When comparing the run time on a query of home-sales on the temporay table created, the cached table query was quicker. One would expect this to occur with the data being loaded from computer memory rather than from distributed nodes.

The parquet and partitioned, on "date_built" column, was loaded across more distributed nodes and generated a similar run time for the query as the cached query.

## Support Received:
* Class Lecture Materials
* Xpert Learning Assistant Chat+
