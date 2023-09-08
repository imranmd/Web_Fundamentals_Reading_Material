# DML Queries in DBMS: A Comprehensive Tutorial

DML (Data Manipulation Language) queries are a crucial part of database management systems (DBMS). They allow you to interact with the data stored in the database by performing operations like inserting, updating, deleting, and querying data. In this tutorial, we'll cover the key DML queries, their purposes, provide sample syntax, and demonstrate their usage with examples.

## List of DML Queries

Here's a list of common DML queries:

1. **INSERT**: Used to add new records into a table.

2. **UPDATE**: Used to modify existing records in a table.

3. **DELETE**: Used to remove records from a table.


## DML Query with Purpose, Syntax, and Example


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

These DML queries allow you to manipulate data within your database, from retrieving specific data using `SELECT` to modifying records with `INSERT`, `UPDATE`, `DELETE`

By mastering these DML queries, you can efficiently manage your data and perform a wide range of operations on it within your DBMS.