# LITA_Class_Project
This a documentation of my learning journey with Ladies in Tech Africa(LITA). My first Data Analysis Project with LITA.

## Project Title:LITA Class

### Project Description
This course provides a comprehensive understanding of  data analysis . 
The course focused on practical, hands-on activities that demonstrate how data analysis skills can be used for real-world data problems.I learnt how to import, clean, analyze, visualize,write SQL queries and interpret data effectively

### Data Source
The sources of Data uses CSV,International Breweries.csv,excel filesand web data which can be accessed by the public.

### Tools Used
- Microsoft Excel [Download here](https://www.microsoft.com/en-us/microsoft-365/previous-versions/microsoft-excel-2013)
  1. For Data Organization
  2. For Data Cleaning and Preprocessing
  3. For Analysis
  4. For Visualizations
  5. For Data Summarization.

- SQL (Structured Query Language) [Download here](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)
  1. For Querying data
  2. For Data Aggregation
  3. For Data Filtering
  4. For Data Manipulation
  5. For Data Integrity Check 
  6. For Data Exporting.
  7.  For Database Management
     
- Github [SignUp here](https://github.com/join)
   1. For Building Portfolio

## Excel
### Data Cleaning and Preprocessing
At the phase of data cleaning and preprocessing, the following actions were performed:
  1. Removing Duplicates: Identification and removal of duplicate entries from datasets, ensuring data integrity.
  2. Handling Missing Values: Rows with missing data were removed.
  3. Data Validation: Data validation rules were set to ensure accurate data entry, such as limiting inputs to specific types, ranges, or predefined lists.
  4. Data Loading
  5. Data Formatting

### Statistical Analysis
Descriptive Statistics: Use of functions (e.g., AVERAGE(), Sum(), STDEV(), MIN(), MAX(), COUNT()) provide key statistical summaries to understand central tendencies and data variability.

### Data Visualization
Conditional Formatting
Sparklines: These tiny in-cell charts provide a simple way to show trends in data over time, directly within a cell, useful for tracking performance metrics.
Dashboards: Excel was used to build interactive dashboards that present key metrics and data visualizations, offering a clear snapshot of business performance.
Data Summarization: Pivot tables allow users to dynamically summarize large datasets, grouping data based on categories or time periods to quickly derive insights.
Customization: Pivot tables can be easily customized with filters, slicers, and calculated fields to answer specific questions or explore different perspectives.
Pivot Charts: Coupled with pivot tables, pivot charts visually represent summarized data, making it easier to understand relationships and trends.

## SQL
1. Data Retrieval (Querying Data)
Selecting Data: SQL allows analysts to retrieve specific data from large datasets using the SELECT statement. You can pull exactly the data needed from one or multiple tables based on specific criteria.
Example: SELECT name, age FROM customers WHERE age > 30;
Filtering Data: Using the WHERE clause, analysts can filter data based on specific conditions, making it easy to extract subsets of data that meet certain criteria.
Example: SELECT * FROM orders WHERE order_date BETWEEN '2024-01-01' AND '2024-01-31';
Sorting Data: SQL allows sorting of results in ascending or descending order using the ORDER BY clause.
Example: SELECT * FROM sales ORDER BY sale_amount DESC;
2. Data Aggregation and Summarization
Aggregating Data: SQL provides powerful aggregation functions such as COUNT(), SUM(), AVG(), MIN(), and MAX() to summarize and analyze data.
Example: SELECT AVG(salary) FROM employees WHERE department = 'Marketing';
Group By Function: The GROUP BY clause allows analysts to group rows that have the same values in specific columns and then apply aggregate functions to each group.
Example: SELECT department, COUNT(*) FROM employees GROUP BY department;
HAVING Clause: This clause allows filtering on aggregated data (after applying the GROUP BY clause).
Example: SELECT department, COUNT(*) FROM employees GROUP BY department HAVING COUNT(*) > 10;
3. Data Filtering and Conditional Logic
Using Logical Operators: SQL’s logical operators such as AND, OR, and NOT allow for advanced filtering of data.
Example: SELECT * FROM products WHERE price > 100 AND category = 'Electronics';
Conditional Logic with CASE Statements: The CASE statement allows analysts to create conditional queries and new computed fields.
Example:
sql
Copy code
SELECT product_name, 
       CASE 
         WHEN price > 100 THEN 'Expensive'
         ELSE 'Affordable'
       END AS price_category
FROM products;
4. Joining Data from Multiple Tables
Inner Join: SQL makes it easy to combine data from multiple related tables using joins. INNER JOIN retrieves only the rows that have matching values in both tables.
Example:
sql
Copy code
SELECT customers.name, orders.order_id 
FROM customers 
INNER JOIN orders ON customers.customer_id = orders.customer_id;
Left Join: A LEFT JOIN retrieves all rows from the left table and the matching rows from the right table, returning NULL for missing matches.
Example:
sql
Copy code
SELECT employees.name, departments.department_name 
FROM employees 
LEFT JOIN departments ON employees.department_id = departments.department_id;
Cross Join: SQL also supports CROSS JOIN, which combines all rows from both tables.
Self Join: A SELF JOIN is used when you need to join a table to itself to compare rows within the same table.
5. Data Transformation and Manipulation
Creating New Columns: SQL can be used to create new computed columns based on existing data. For example, analysts can derive new fields like total sales or profit.
Example: SELECT price * quantity AS total_sales FROM orders;
String Manipulation: SQL provides functions like CONCAT(), SUBSTRING(), UPPER(), LOWER(), and TRIM() to clean and manipulate string data.
Example: SELECT CONCAT(first_name, ' ', last_name) AS full_name FROM employees;
Date Functions: SQL includes various functions to manipulate dates (DATEADD(), DATEDIFF(), YEAR(), MONTH()) which are often critical for time-based analysis.
Example: SELECT order_id, DATEDIFF(day, order_date, delivery_date) AS delivery_time FROM orders;
6. Data Integrity and Quality Checks
Identifying Duplicates: SQL can easily identify and remove duplicates using the DISTINCT keyword or by finding duplicate entries based on specific columns.
Example: SELECT DISTINCT customer_id FROM orders;
Checking for Missing Data: SQL can be used to detect missing or incomplete data using IS NULL or IS NOT NULL conditions.
Example: SELECT * FROM customers WHERE email IS NULL;
Data Validation: SQL helps in ensuring data quality through validation checks such as applying constraints (UNIQUE, NOT NULL, CHECK) to the dataset.
7. Subqueries and Nested Queries
Subqueries: SQL allows you to run queries inside other queries. Subqueries can be used to filter data dynamically or compare values across datasets.
Example:
sql
Copy code
SELECT * FROM employees 
WHERE salary > (SELECT AVG(salary) FROM employees);
Correlated Subqueries: In correlated subqueries, the inner query depends on the outer query, which is useful for advanced filtering and comparisons.
Example:
sql
Copy code
SELECT e1.name, e1.salary 
FROM employees e1 
WHERE e1.salary > (SELECT AVG(e2.salary) FROM employees e2 WHERE e2.department = e1.department);
8. Creating and Modifying Data Models
Table Creation: SQL enables analysts to create new tables in a database to store specific datasets for analysis or reporting.
Example:
sql
Copy code
CREATE TABLE new_sales_data (
    sale_id INT PRIMARY KEY,
    product_id INT,
    sale_amount DECIMAL(10, 2)
);
Inserting Data: You can insert new rows into existing tables using SQL.
Example: INSERT INTO employees (name, age, department) VALUES ('John', 30, 'Marketing');
Updating Data: SQL allows data modifications to update existing records, which is useful for correcting data errors or making adjustments.
Example: UPDATE products SET price = price * 1.1 WHERE category = 'Electronics';
Deleting Data: Analysts can use SQL to delete irrelevant or outdated data.
Example: DELETE FROM customers WHERE customer_id = 10;
9. Time Series Analysis
Date Filtering: SQL’s WHERE clause can filter time-based data, allowing for the analysis of trends over days, months, or years.
Example: SELECT SUM(sales_amount) FROM sales WHERE order_date BETWEEN '2023-01-01' AND '2023-12-31';
Time-Based Aggregation: SQL can group data by date (daily, monthly, yearly) to analyze trends over time.
Example: SELECT EXTRACT(YEAR FROM order_date), SUM(sales_amount) FROM sales GROUP BY EXTRACT(YEAR FROM order_date);
