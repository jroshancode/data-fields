<img width="1102" height="583" alt="image" src="https://github.com/user-attachments/assets/69e2e883-d749-4bcc-a98a-7dc0476adf6f" />

#2025 - 08 - 23 

Create a table Orders with: <br>
OrderID (integer, primary key) <br>
OrderDate (DATE) <br>
OrderTime (TIME) <br>
CreatedAt (DATETIME, default current date/time) <br>

Create a table Products with the following: <br>
ProductID (integer, primary key) <br>
Price (decimal, 2 decimal places) <br>
Stock (integer, default 0) <br>


#2025 - 08 - 26 

What is DDL? List some common DDL commands.

    DDL stands for Data Definition Language, used to define, modify, and manage the structure of database objects. Common DDL commands are:
    CREATE: To create new tables, views, indexes, etc.
  
    ALTER: To modify existing database structures, such as adding columns to a table.
    DROP: To delete objects, like tables or indexes.
    TRUNCATE: To quickly remove all records from a table without logging each row deletion.
    RENAME: To rename a database object, such as a table or column.

2. Explain the purpose and usage of the CREATE TABLE statement.
    The CREATE TABLE statement is used to define a new table in a database.
    It specifies the table name, column names, data types, and constraints (e.g., primary key, foreign key, not null).
    Example: -
    CREATE TABLE employees (
      id INT PRIMARY KEY,
      name VARCHAR(50), 
      salary DECIMAL(10,2)
    );

    CREATE TABLE Employees (
        EmployeeID INT PRIMARY KEY,
        FirstName VARCHAR(50),
        LastName VARCHAR(50),
        BirthDate DATE
    );

3. What are constraints? Name a few and explain their usage.
    Constraints enforce rules on data in a table. Some common constraints are:
    PRIMARY KEY: Uniquely identifies each record.
    FOREIGN KEY: Enforces a relationship between two tables.
    UNIQUE: Ensures all values in a column are unique.
    CHECK: Restricts values based on a condition.
    NOT NULL: Ensures that a column cannot have NULL values.

4. What is the difference between ALTER TABLE and DROP TABLE statements?
    ALTER TABLE is used to modify the structure of an existing table, such as adding/removing columns, modifying data types, or adding/removing constraints.
    DROP TABLE is used to completely remove a table and its data from the database.
    Example ALTER TABLE: ALTER TABLE employees ADD email VARCHAR(50);
    Example DROP TABLE: DROP TABLE employees;

5. Explain the purpose and usage of the TRUNCATE TABLE statement.
    TRUNCATE TABLE is used to quickly remove all rows from a table, while preserving the table structure.
    It is faster than using a DELETE statement without a WHERE clause, as TRUNCATE does not generate transaction logs.
    Example: TRUNCATE TABLE orders;

6. What is the difference between DROP TABLE and TRUNCATE TABLE?
    DROP TABLE removes the table definition and all its data from the database.
    TRUNCATE TABLE removes all the data from the table, but the table structure (columns, constraints, etc.) remains.
    DROP TABLE is a DDL operation, while TRUNCATE TABLE is a DML (Data Manipulation Language) operation.
    DROP TABLE is irreversible, while TRUNCATE TABLE can be rolled back within a transaction.

7. What is the difference between DELETE, TRUNCATE, and DROP?
    DELETE: Deletes specific rows from a table. It can be rolled back and generates a log.
    TRUNCATE: Removes all rows from a table without logging each row, so it’s faster but cannot be rolled back.
    DROP: Deletes an entire database object (like a table), along with its structure. It is also non-reversible.
