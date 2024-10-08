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
### Creating and Modifying Data Models
- Table Creation: SQL was used to create new tables in a database to store specific datasets for analysis or reporting.
Example: CREATE TABLE Employee (
staffid varchar (10) not null,
FirstName varchar (255) NOT NULL,
SecondName varchar (255),
Gender varchar (10),
Date_of_Birth date,
HireDate datetime,
primary key (staffid))

- Inserting Data: 
Example: insert into Employee (staffid, firstname, secondname, gender,Date_of_Birth, hiredate)
values ( 'AB401', 'ayan', 'olakun', 'female', '1992-08-22', '2018-02-09'),
( 'AB212', 'okorie', 'mercy', 'female','1988-10-09', '2018-10-09'),
( 'AB223', 'joshua', 'chukwuemeka', 'male','1980-10-09', '2022-02-09'),
( 'AB234', 'sanni', 'ibrahim', 'male','1958-10-09', '2019-09-23'),
( 'AB254', 'mercy', 'olanipekun', 'female','1982-10-09', '2020-02-09'),
( 'AB249', 'johnson', 'mercy', 'female','1982-10-09', '2019-12-09'),
( 'AB298', 'ayomide', 'halleluyah', 'female', '1982-10-09','2018-07-11'),
( 'AB260', 'deborah', 'justin', 'female','1982-10-09', '2018-02-09'),
( 'AB281', 'wale', 'olanipekun', 'male','1982-10-09', '2018-02-09')

- Updating Data: To update existing records, which is useful for correcting data errors or making adjustments.
Example: insert into [dbo].[Employee]
values ( 'AB200', 'ayomide', 'halleluyah', 'female', '1982-10-09','2018-07-11')

- Deleting Data: To delete irrelevant or outdated data.
Example: delete from employee
where staffid  = 'ab281'

### Data Retrieval (Querying Data)
- Selecting Data: To retrieve specific data from large datasets using the SELECT statement. You can pull exactly the data needed from one or multiple tables based on specific criteria.
    Example: select * from Employee;
  
- Filtering Data: Using the WHERE clause, to filter data based on specific conditions, making it easy to extract subsets of data that meet certain criteria.
Example: SELECT * FROM Salary
WHERE Staffid = 'AB281';

- Sorting Data: SQL allows sorting of results in ascending or descending order using the ORDER BY clause.
Example: SELECT * FROM sales ORDER BY sale_amount DESC;

###Data Aggregation and Summarization
- Aggregating Data: Aggregation functions such as COUNT(), SUM(), AVG(), MIN(), and MAX() were used to summarize and analyze data.
Example: SELECT AVG(salary) AS AVERAGESALARY FROM Salary

- Group By Function: The GROUP BY clause was used to group rows that have the same values in specific columns and then apply aggregate functions to each group.
Example: SELECT department, COUNT(*) FROM employees GROUP BY department;

- HAVING Clause: This clause allows filtering on aggregated data (after applying the GROUP BY clause).
Example: SELECT department, COUNT(*) FROM employees GROUP BY department HAVING COUNT(*) > 10;

### Data Filtering and Conditional Logic
- Using Logical Operators: SQL’s logical operators such as AND, OR, and NOT for advanced filtering of data.
Example: SELECT * FROM products WHERE price > 100 AND category = 'Electronics';

- Joining Data from Multiple Tables
    1. Inner Join: INNER JOIN retrieves only the rows that have matching values in both tables.
Example:select employee.staffid,
           employee.firstname, 
		   employee.gender,
		   employee.hiredate,
			employee.state_of_origin,
			Salary.department,
			 Salary.salary,
			 Payment.Account_No,
			 Payment.Bank,
			 Payment.Payment_Method
from employee
inner join Salary
on salary.Staffid = employee.staffid
inner join Payment
on Payment.staffid = salary.Staffid

   2. Left Join: A LEFT JOIN retrieves all rows from the left table and the matching rows from the right table, returning NULL for missing matches.
Example: select employee.staffid, employee.firstname, employee.gender,
			 employee.hiredate,employee.state_of_origin, Salary.department,
			 Salary.salary
     from employee
     left join Salary
     on salary.Staffid = employee.staffid
    
### Data Integrity and Quality Checks
- Identifying Duplicates: SQL can easily identify and remove duplicates using the DISTINCT keyword or by finding duplicate entries based on specific columns.
Example: SELECT DISTINCT customer_id FROM orders;
- Checking for Missing Data: SQL can be used to detect missing or incomplete data using IS NULL or IS NOT NULL conditions.
Example: SELECT * FROM customers WHERE email IS NULL;
- Data Validation: Ensuring data quality through validation checks such as  (UNIQUE, NOT NULL, CHECK) to the dataset.


