# DML Queries in DBMS: A Comprehensive Tutorial

DML (Data Manipulation Language) queries are a crucial part of database management systems (DBMS). They allow you to interact with the data stored in the database by performing operations like inserting, updating, deleting, and querying data. In this tutorial, we'll cover the key DML queries, their purposes, provide sample syntax, and demonstrate their usage with examples.

## List of DML Queries

Here's a list of common DML queries:

1. **SELECT**: Used to retrieve data from one or more tables.

2. **INSERT**: Used to add new records into a table.

3. **UPDATE**: Used to modify existing records in a table.

4. **DELETE**: Used to remove records from a table.

5. **MERGE**: Used to perform conditional insert, update, or delete operations based on a specified condition.

## DML Query with Purpose, Syntax, and Example

### 1. SELECT

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

### 2. INSERT

**Purpose**: To add new records into a table.

**Syntax**:
```sql
INSERT INTO table_name (column1, column2, ...)
VALUES (value1, value2, ...);
```

**Example**:
```sql
-- Insert a new employee record
INSERT INTO Employees (EmployeeID, FirstName, LastName, Salary)
VALUES (101, 'John', 'Doe', 60000);
```

### 3. UPDATE

**Purpose**: To modify existing records in a table.

**Syntax**:
```sql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```

**Example**:
```sql
-- Update the salary of an employee
UPDATE Employees
SET Salary = 65000
WHERE EmployeeID = 101;
```

### 4. DELETE

**Purpose**: To remove records from a table.

**Syntax**:
```sql
DELETE FROM table_name
WHERE condition;
```

**Example**:
```sql
-- Delete an employee record
DELETE FROM Employees
WHERE EmployeeID = 101;
```

### 5. MERGE (Conditional Upsert)

**Purpose**: To perform conditional insert, update, or delete operations based on a specified condition.

**Syntax**:
```sql
MERGE INTO target_table AS T
USING source_table AS S
ON T.matching_column = S.matching_column
WHEN MATCHED THEN
    UPDATE SET T.column1 = S.column1, T.column2 = S.column2, ...
WHEN NOT MATCHED THEN
    INSERT (column1, column2, ...)
    VALUES (S.column1, S.column2, ...);
```

**Example**:
```sql
-- Merge data from source_table into target_table based on a matching column
MERGE INTO Employees AS T
USING NewEmployees AS S
ON T.EmployeeID = S.EmployeeID
WHEN MATCHED THEN
    UPDATE SET T.Salary = S.Salary
WHEN NOT MATCHED THEN
    INSERT (EmployeeID, FirstName, LastName, Salary)
    VALUES (S.EmployeeID, S.FirstName, S.LastName, S.Salary);
```

These DML queries allow you to manipulate data within your database, from retrieving specific data using `SELECT` to modifying records with `INSERT`, `UPDATE`, `DELETE`, and performing conditional operations with `MERGE`.

By mastering these DML queries, you can efficiently manage your data and perform a wide range of operations on it within your DBMS.