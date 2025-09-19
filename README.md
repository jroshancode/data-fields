<img width="1102" height="583" alt="image" src="https://github.com/user-attachments/assets/69e2e883-d749-4bcc-a98a-7dc0476adf6f" />

W3schools:- [ https://www.w3schools.com/sql/sql_exercises.asp] <br>
Codechef:- [ https://www.codechef.com/practice/sql-case-studies-topic-wise] <br> 
hackerrank:- [ https://www.hackerrank.com/domains/sql ] <br> 
sqlzoo  :- [https://sqlzoo.net/wiki/SQL_Tutorial ] <br> 
Geeksforgeeks :- [ https://www.geeksforgeeks.org/sql/sql-exercises/] <br> 
Leetcode :- https://leetcode.com/studyplan/top-sql-50/<br> 


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


#2025 - 08 - 30 

create table business( <Br>
id int primary key auto_increment, <Br>
name varchar(20) not null, <Br>
email varchar(50) not null, <Br>
password varchar(20) not null, <Br>
user_name varchar(20) not null unique, <Br>
address varchar(40),  <Br>
salary int not null);  <Br>

insert into business(name,email,password,user_name,address,salary) <Br>
values("ankit","ankit@gmail.com","a123","ank123","street road",15000), <Br>
    ("Mohit",null,"b123","mus123","mumbai",20000), <Br>
    ("raunak","c@gmail.com",null,"rau123","delhi",10000); <Br>
    
    
insert into business(name,email,password,user_name,salary) <Br>
values("A","a@gmail.com","a123","ank123",15000), <Br>
    ("B","b@gmail.com",null,"mus123",20000), <Br>
    ("C","c@gmail.com","c123","rau123",null); <Br>



create table product( <Br>
p_id int primary key auto_increment, <Br>
name varchar(30) not null, <Br>
category varchar(30) not null unique, <Br>
quantity int, <Br>
price float not null); <Br>

insert into product(name,category,quantity,price) <Br>
values("laptop","i3",2,80000), <Br>
("headphones","boat",1,5000), <Br>
("monitor","zebronics",3,25000), <Br>
("LED",null,3,25000);  <Br>

insert into product(name,category,quantity,price) <Br>
values("laptop","i3",2,80000), <Br>
("headphones","boat",1,5000),  <Br>
("monitor","",3,25000);   <Br>
 

-- Apply count and order by for read following these two tables data.  <Br>
select * from product;  <Br>

select  * from business; <Br>



Create a table Students with: StudentID (integer, primary key) <br>
Name (NOT NULL)  <br>
Age (integer, must be >= 18)  <br>
Email (must be unique)  <br>
EnrolledDate (default current date)  <br>
Create a table Employees with:  <br>
EmpID (integer, primary key)  <br>
Name (VARCHAR)  <br>
ManagerID (integer, nullable)  <br>

// Create table and insert any five records

# 2025 - 09 - 02 
1. What is SQL or Why SQL ?
2. What is different between Entity or attribute or tuples of records ?
3. What is Database Schemas ?
4. What is Server or Database ?
5. What is a primary key, and why is it important?
6. What is the difference between a primary key and a foreign key?
7. Explain the difference between DELETE, TRUNCATE, and DROP.
8. What are SQL constraints? Provide examples (e.g., NOT NULL, UNIQUE, CHECK).
9. suppose Amazon has stored much information about customers, products, orders, categories or more in the database tables. Customers want to change their information, which Sql commands should you use to solve this problem?
I have users or posts tables and I want a relationship between both tables and get information, so what is your approach, and how do you solve this problem ?

# 2025 - 09 - 03 
1. How to Create a Database abc if this database have already exists ?
2. Write a command to display all database name ?
3. Created Students table with id,s_name, age, email, phone and address attributes makes sure id is primary key and any columns have never store null values?
4. What is output of the code ( select * from students )
5. Explane this SQL query ( Truncate table ABC; )
6. What is the advantages or disadvantages of using drop commands ?
7. 

# 2025 - 09 - 12 
<img width="599" height="415" alt="image" src="https://github.com/user-attachments/assets/aa48f043-ea53-4278-a8b1-ce693ae94512" />


# 2025 - 09 - 19 
CHAR stores fixed-length strings, padding shorter values with spaces to reach the specified length, which can be faster for consistent-length data but wastes space. VARCHAR stores variable-length strings, only using the space for the actual characters plus some overhead for length information. Use CHAR for consistent data like state abbreviations and VARCHAR for variable data like names or addresses

<img width="599" height="415" alt="image" src="https://github.com/user-attachments/assets/c77c7508-217e-4d24-b5ff-b619febb99ed" />


