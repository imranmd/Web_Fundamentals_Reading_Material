Data Transaction Language (DTL) queries in DBMS are used to manage database transactions. A transaction is a sequence of one or more SQL statements that are executed as a single unit of work. DTL queries ensure that transactions are executed in a way that maintains data consistency and integrity, even in the presence of failures. In this tutorial, we'll cover the key DTL queries, their purposes, provide sample syntax, and demonstrate their usage with examples.

**List of DTL Queries**

Here's a list of common DTL queries:

1. **BEGIN TRANSACTION / START TRANSACTION**: Initiates a new transaction.

2. **COMMIT**: Confirms the changes made during a transaction, making them permanent.

3. **ROLLBACK**: Undoes the changes made during a transaction, reverting to the previous state.

4. **SAVEPOINT**: Sets a savepoint within a transaction to which you can later roll back.

**DTL Query with Purpose, Syntax, and Example**

**1. BEGIN TRANSACTION / START TRANSACTION**

**Purpose**: Initiates a new transaction.

**Syntax**:
```sql
BEGIN TRANSACTION;
-- or
START TRANSACTION;
```

**Example**:
```sql
BEGIN TRANSACTION;
-- SQL statements for data manipulation
COMMIT;
```

**2. COMMIT**

**Purpose**: Confirms the changes made during a transaction, making them permanent.

**Syntax**:
```sql
COMMIT;
```

**Example**:
```sql
BEGIN TRANSACTION;
-- SQL statements for data manipulation
COMMIT;
```

**3. ROLLBACK**

**Purpose**: Undoes the changes made during a transaction, reverting to the previous state.

**Syntax**:
```sql
ROLLBACK;
```

**Example**:
```sql
BEGIN TRANSACTION;
-- SQL statements for data manipulation
ROLLBACK;
```

**4. SAVEPOINT**

**Purpose**: Sets a savepoint within a transaction to which you can later roll back.

**Syntax**:
```sql
SAVEPOINT savepoint_name;
```

**Example**:
```sql
BEGIN TRANSACTION;
-- SQL statements for data manipulation
SAVEPOINT before_update;
-- More SQL statements
ROLLBACK TO before_update;
-- This will undo changes made after the savepoint
COMMIT;
```

These DTL queries are essential for managing the integrity and consistency of data within a database. Transactions ensure that a series of operations either complete successfully or leave the database in a consistent state if an error occurs.

By mastering these DTL queries, you can effectively manage and control transactions within your DBMS, ensuring data integrity and reliability.