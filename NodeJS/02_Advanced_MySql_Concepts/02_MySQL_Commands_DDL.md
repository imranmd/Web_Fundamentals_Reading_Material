# Categories of MySQL commands : Comprehensive guide

These categories encompass the various MySQL commands used for querying, modifying, defining, controlling, and managing databases and their data. Depending on your specific use case, you'll use these commands to interact with your MySQL database effectively.

![Data Types](../Assets/Database%20Commands.png)

- **Data Querying Commands**:
  - **SELECT**: Retrieve data from one or more tables.
  - **FROM**: Specify the table(s) to query.
  - **WHERE**: Filter data based on specified conditions.
  - **GROUP BY**: Group rows based on one or more columns.
  - **HAVING**: Filter grouped data based on conditions.
  - **ORDER BY**: Sort the result set by one or more columns.
  - **LIMIT**: Limit the number of rows returned in the result.

- **Data Modification Commands**:
  - **INSERT INTO**: Add new rows into a table.
  - **UPDATE**: Modify existing rows in a table.
  - **DELETE**: Remove rows from a table.
  - **REPLACE**: Insert a new row or replace an existing one based on a unique key.
  - **INSERT IGNORE**: Insert a new row, ignoring duplicate key errors.
  - **TRUNCATE**: Delete all rows from a table, but retain the table structure.

- **Data Definition Commands**:
  - **CREATE DATABASE**: Create a new database.
  - **DROP DATABASE**: Delete an existing database.
  - **CREATE TABLE**: Create a new table with specified columns and data types.
  - **ALTER TABLE**: Modify the structure of an existing table.
  - **DROP TABLE**: Delete an existing table and its data.
  - **INDEX**: Create an index on one or more columns for faster data retrieval.

- **Data Control Commands**:
  - **GRANT**: Assign specific privileges to database users.
  - **REVOKE**: Remove specific privileges from database users.
  - **CREATE USER**: Create a new database user.
  - **ALTER USER**: Modify an existing user's properties.
  - **DROP USER**: Delete an existing database user.

- **Database Management Commands**:
  - **SHOW DATABASES**: Display a list of all available databases.
  - **USE**: Select a specific database for subsequent operations.
  - **SHOW TABLES**: Show a list of tables in the current database.
  - **SHOW COLUMNS**: Display the columns of a table.
  - **DESCRIBE or EXPLAIN**: Provide information about the structure of a table.
  
- **Transaction Control Commands**:
  - **BEGIN**: Start a new transaction.
  - **COMMIT**: Save the changes made in the current transaction.
  - **ROLLBACK**: Undo the changes made in the current transaction.
  - **SAVEPOINT**: Set a savepoint within a transaction.
  - **ROLLBACK TO**: Rollback to a specific savepoint.
  
- **User-Defined Functions (UDF)**:
  - MySQL allows you to create your own user-defined functions in supported programming languages.

- **System Commands**:
  - Commands related to server administration, configuration, and maintenance.



# DDL Queries in MySQL: A Comprehensive Tutorial

DDL (Data Definition Language) queries are a fundamental part of database management systems (DBMS). They are used to define, modify, and manage the structure and properties of database objects such as tables, indexes, and constraints. In this comprehensive tutorial, we'll cover the key DDL queries, their purposes, provide sample syntax, and demonstrate their usage with examples.

## List of DDL Queries

Here's a list of common DDL queries:

1. **CREATE TABLE**: Used to create a new table in the database.

2. **ALTER TABLE**: Used to modify the structure of an existing table.

3. **DROP TABLE**: Used to delete a table and all its data from the database.

4. **CREATE INDEX**: Used to create an index on one or more columns of a table for faster data retrieval.

5. **DROP INDEX**: Used to delete an index from the database.

6. **CREATE DATABASE**: Used to create a new database within the DBMS.

7. **ALTER DATABASE**: Used to modify database properties or settings.

8. **DROP DATABASE**: Used to delete an entire database, including all its tables and data.

## DDL Query with Purpose, Syntax, and Example

### 1. CREATE TABLE

**Purpose**: To create a new table in the database.

**Syntax**:
```sql
CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    ...
);
```

**Example**:
```sql
CREATE TABLE Employees (
    EmployeeID INT PRIMARY KEY,
    FirstName VARCHAR(50),
    LastName VARCHAR(50),
    Department VARCHAR(50)
);
```

### 2. ALTER TABLE

**Purpose**: To modify the structure of an existing table (e.g., add, modify, or delete columns).

**Syntax**:
```sql
ALTER TABLE table_name
    ADD column_name datatype;

ALTER TABLE table_name
    MODIFY column_name new_datatype;

ALTER TABLE table_name
    DROP COLUMN column_name;
```

**Example**:
```sql
-- Add a new column
ALTER TABLE Employees
    ADD Email VARCHAR(100);

-- Modify the data type of a column
ALTER TABLE Employees
    MODIFY DepartmentCode INT;

-- Delete a column
ALTER TABLE Employees
    DROP COLUMN LastName;
```

### 3. DROP TABLE

**Purpose**: To delete a table and all its data from the database.

**Syntax**:
```sql
DROP TABLE table_name;
```

**Example**:
```sql
DROP TABLE Employees;
```

### 4. CREATE INDEX

**Purpose**: To create an index on one or more columns of a table for faster data retrieval.

**Syntax**:
```sql
CREATE INDEX index_name
ON table_name (column1, column2, ...);
```

**Example**:
```sql
CREATE INDEX idx_employee_id
ON Employees (EmployeeID);
```

### 5. DROP INDEX

**Purpose**: To delete an index from the database.

**Syntax**:
```sql
DROP INDEX index_name;
```

**Example**:
```sql
DROP INDEX idx_employee_id;
```

### 6. CREATE DATABASE

**Purpose**: To create a new database within the DBMS.

**Syntax**:
```sql
CREATE DATABASE database_name;
```

**Example**:
```sql
CREATE DATABASE MyNewDatabase;
```

### 7. ALTER DATABASE

**Purpose**: To modify database properties or settings.

**Syntax**:
```sql
ALTER DATABASE database_name
    SET property_name = new_value;
```

**Example**:
```sql
-- Change the collation of a database
ALTER DATABASE MyDatabase
    SET COLLATE SQL_Latin1_General_CP1_CI_AS;
```

### 8. DROP DATABASE

**Purpose**: To delete an entire database, including all its tables and data.

**Syntax**:
```sql
DROP DATABASE database_name;
```

**Example**:
```sql
DROP DATABASE MyDatabase;
```

These DDL queries are essential for defining and managing the structure of your database objects. By understanding their purpose and usage, you can efficiently create, modify, and maintain your database schema in a DBMS.
## Summary

In this comprehensive guide, we've explored MySQL's Data Definition Language (DDL), understanding its concepts and practical applications. By grasping the key DDL commands for creating databases, tables, indexes, and views, you're empowered to define and manage your database structure effectively. As you work on developing and maintaining databases, the knowledge of DDL in MySQL will serve as a foundational skill in building robust and well-structured data systems.