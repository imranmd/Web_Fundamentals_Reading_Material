Data Query Language (DQL) queries in a Database Management System (DBMS) are used to retrieve and manipulate data from a database. DQL is primarily concerned with querying and retrieving data from database tables. In this tutorial, we'll provide a list of common DQL queries, explain their purpose, and provide sample syntax and examples.

**List of DQL Queries Example**

Here's a list of common DQL queries:

**SELECT**: Used to retrieve data from one or more tables.

**DQL Query with Purpose, Syntax, and Examples**

**1. SELECT**

**Purpose**: To retrieve data from one or more tables.

**Syntax**:
```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```

**Example**:
```sql
-- Retrieve all employees' names and salaries from the Employees table
SELECT FirstName, LastName, Salary
FROM Employees;
```

```sql
-- Retrieve employees who belong to the 'HR' department
SELECT *
FROM Employees
WHERE Department = 'HR';
```

```sql
-- Retrieve the total number of employees
SELECT COUNT(*)
FROM Employees;
```

```sql
-- Calculate the average salary of employees
SELECT AVG(Salary)
FROM Employees;
```

```sql
-- Retrieve employees sorted by salary in descending order
SELECT EmployeeID, FirstName, LastName, Salary
FROM Employees
ORDER BY Salary DESC;
```

```sql
-- Retrieve unique departments in the organization
SELECT DISTINCT Department
FROM Employees;
```

These DQL queries are essential for retrieving data from a database, performing calculations, and obtaining meaningful insights from your data. By mastering these DQL queries, you can efficiently query and manipulate data within your DBMS.