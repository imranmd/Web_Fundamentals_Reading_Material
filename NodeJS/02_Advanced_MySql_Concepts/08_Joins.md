# Joins in MySQL: A Comprehensive Tutorial

Joins in MySQL allow you to combine rows from two or more tables based on a related column between them. This tutorial covers various types of joins, their purposes, and provides sample syntax and examples.

![MySQL Joins](../Assets/SQL%20Join.png)


## Types of Joins

Here are some common types of joins in MySQL:

1. **INNER JOIN**: Returns only the rows where there is a match in both tables.
2. **LEFT JOIN (or LEFT OUTER JOIN)**: Returns all rows from the left table and the matched rows from the right table. The result contains unmatched rows from the left table as well.
3. **RIGHT JOIN (or RIGHT OUTER JOIN)**: Returns all rows from the right table and the matched rows from the left table. The result contains unmatched rows from the right table as well.
4. **FULL JOIN (or FULL OUTER JOIN)**: Returns all rows when there is a match in either the left or right table.
5. **CROSS JOIN**: Returns the Cartesian product of rows from both tables (all possible combinations).
6. **SELF JOIN**: Joins a table with itself, typically to find relationships between rows within the same table.
7. **UNION JOIN**: Combines the results of two SELECT statements into a single result set.

## Joins with Purpose, Syntax, and Example

### 1. INNER JOIN

**Purpose**: To return only the rows where there is a match in both tables.

**Syntax**:
```sql
SELECT columns
FROM table1
INNER JOIN table2
ON table1.column = table2.column;
```

**Example**:
```sql
-- Retrieve a list of orders and their corresponding customers
SELECT Orders.OrderID, Customers.CustomerName
FROM Orders
INNER JOIN Customers
ON Orders.CustomerID = Customers.CustomerID;
```

### 2. LEFT JOIN (LEFT OUTER JOIN)

**Purpose**: To return all rows from the left table and matched rows from the right table. Unmatched rows from the left table will contain NULL values for right table columns.

**Syntax**:
```sql
SELECT columns
FROM table1
LEFT JOIN table2
ON table1.column = table2.column;
```

**Example**:
```sql
-- Retrieve a list of all employees and their assigned departments
SELECT Employees.EmployeeName, Departments.DepartmentName
FROM Employees
LEFT JOIN Departments
ON Employees.DepartmentID = Departments.DepartmentID;
```

### 3. RIGHT JOIN (RIGHT OUTER JOIN)

**Purpose**: To return all rows from the right table and matched rows from the left table. Unmatched rows from the right table will contain NULL values for left table columns.

**Syntax**:
```sql
SELECT columns
FROM table1
RIGHT JOIN table2
ON table1.column = table2.column;
```

**Example**:
```sql
-- Retrieve a list of all products and their associated suppliers
SELECT Products.ProductName, Suppliers.SupplierName
FROM Products
RIGHT JOIN Suppliers
ON Products.SupplierID = Suppliers.SupplierID;
```

### 4. FULL JOIN (FULL OUTER JOIN)

**Purpose**: To return all rows when there is a match in either the left or right table.

**Syntax**:
```sql
SELECT columns
FROM table1
FULL JOIN table2
ON table1.column = table2.column;
```

**Example**:
```sql
-- Retrieve a list of all employees and their assigned departments, including unmatched records
SELECT Employees.EmployeeName, Departments.DepartmentName
FROM Employees
FULL JOIN Departments
ON Employees.DepartmentID = Departments.DepartmentID;
```

### 5. CROSS JOIN

**Purpose**: To return the Cartesian product of rows from both tables (all possible combinations).

**Syntax**:
```sql
SELECT columns
FROM table1
CROSS JOIN table2;
```

**Example**:
```sql
-- Retrieve all possible combinations of products and suppliers
SELECT Products.ProductName, Suppliers.SupplierName
FROM Products
CROSS JOIN Suppliers;
```

### 6. SELF JOIN

**Purpose**: To join a table with itself, typically to find relationships between rows within the same table.

**Syntax**:
```sql
SELECT columns
FROM table1 AS t1
JOIN table1 AS t2
ON t1.column = t2.column;
```

**Example**:
```sql
-- Retrieve a list of employees and their managers from the same Employees table
SELECT e.EmployeeName, m.EmployeeName AS ManagerName
FROM Employees AS e
LEFT JOIN Employees AS m
ON e.ManagerID = m.EmployeeID;
```

### 7. NATURAL JOIN (Not Recommended)

**Purpose**: To perform a join based on columns with the same name in both tables. However, this is not recommended due to potential ambiguity.

**Syntax**:
```sql
SELECT columns
FROM table1
NATURAL JOIN table2;
```

**Example**:
```sql
-- Avoid using NATURAL JOIN as it can lead to ambiguous results
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
NATURAL JOIN Orders;
```

### 8. UNION JOIN

**Purpose**: To combine the results of two SELECT statements into a single result set.

**Syntax**:
```sql
SELECT columns
FROM table1
WHERE condition1
UNION
SELECT columns
FROM table2
WHERE condition2;
```

**Example**:
```sql
-- Retrieve a list of employees and customers who placed orders
SELECT EmployeeName AS Name
FROM Employees
UNION
SELECT CustomerName AS Name
FROM Customers
WHERE CustomerName IS NOT NULL;
```

These join types in MySQL allow you to retrieve data from multiple tables based on relationships between them. Depending on your specific data retrieval needs, you can choose the appropriate join type to construct the desired result set.