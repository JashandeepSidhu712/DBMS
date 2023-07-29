# DATABASE LANGUAGES

## DDL COMMANDS

DDL or **Data Definition Language** actually consists of the SQL commands that can be used to **define the database schema**. <br>
DDL is a set of SQL commands used to create, modify, and delete database structures but not data. 

**CREATE** <br>
This command is used to create the database or its objects (like table, index, function, views, store procedure, and triggers).

**DROP** <br>
This command is used to delete objects from the database.

**ALTER** <br>
This is used to alter the structure of the database.

**TRUNCATE** <br>
This is used to remove all records from a table, including all spaces allocated for the records.

**COMMENT** <br>
This is used to add comments to the data dictionary.

**RENAME** <br>
This is used to rename an object existing in the database.


### Queries for DDL commands

**create database** <br>
CREATE database database_name;

**view all databases created in system** <br>
SHOW databases;

**use database** <br>
USE database_name;

**create table with columns in it** <br>
CREATE table table_name(Column1 datatype (size), column2 datatype (size), PRIMARY KEY (column));

**drop table** <br>
DROP TABLE table_name;

**drop database** <br>
DROP DATABASE database_name;

**add columns into the existing table** <br>
ALTER TABLE table_name ADD (Columnname_1  datatype, Columnname_2  datatype);

**drop column in a table** <br>
ALTER TABLE table_name DROP COLUMN column_name;

**rename table name** <br>
ALTER TABLE table_name RENAME TO new_table_name;

**rename columns name** <br>
ALTER TABLE table_name RENAME COLUMN old_name TO new_name;


**DROP vs TRUNCATE vs DELETE** <br>
Truncate preserves the structure of the table for future use, deletes only the data from the structure. <br>
Whereas, drop tables where the table is deleted with its full structure and the data. <br>
The DELETE Statement in SQL is used to delete existing records from a table. We can delete a single record or multiple records depending on the condition we specify in the WHERE clause.

**To delete the whole database** <br>
DROP DATABASE student_data; <br>
After running the above query the whole database will be deleted

**To truncate Student_details table from student_data database** <br>
TRUNCATE TABLE Student_details; <br>
After running the above query the data will be deleted but the structure will remain in the memory for further operations

## DQL COMMANDS

DQL statements are used for **performing queries on the data within schema objects**. <br>
We can define DQL as follows: it is a component of SQL that allows getting data from the database and imposing order upon it.

It includes the SELECT statement. This command allows getting the data out of the database to perform operations with it. When a SELECT is fired against a table or tables the result is compiled into a further temporary table, which is displayed or perhaps received by the program i.e. a front-end.

**SELECT** <br>
It is used to retrieve data from the database.

### Queries for DQL Commands

**To fetch the entire table or all the fields in the table** <br>
 SELECT * FROM table_name;

**Query to fetch the particular column from the table Student** <br>
SELECT column1, column3 FROM table_name;

**copy all the data of a table and insert it into a different table** <br>
INSERT INTO first_table SELECT * FROM second_table;

**copy only those columns of a table which we want to insert into a different table** <br>
INSERT INTO first_table(columns1) SELECT columns2 FROM second_table;

**copy specific rows from a table to insert into another table by using WHERE appropriate condition**
INSERT INTO table1 SELECT * FROM table2 WHERE condition;

## DML COMMANDS

The SQL commands that **deal with the manipulation of data present in the database** belong to DML or **Data Manipulation Language** and this includes most of the SQL statements. 

It is the component of the SQL statement that controls access to data and to the database. Basically, DCL statements are grouped with DML statements.

**INSERT** <br>
It is used to insert data into a table.

**UPDATE** <br>
It is used to update existing data within a table.

**DELETE** <br> 
It is used to delete records from a database table.

**LOCK** 
Table control concurrency.

### Queries for DML Commands

**adds data in specific column, (like Column1=Value1)** <br>
Insert into Table_name(Column1, Column2, Column3) Values (Value1, value2, value3);

**adds data in table in sequence of column name(Value1 will be added in Column1.. so on)** <br>
Insert into Table_name Values (Value1, value2, value3);

**Adding multiple data in the table in one go** <br>
Insert into Table_name Values (Value01, value02, value03), (Value11, value12, value13);

**update values where condition meets** <br>
UPDATE table_name SET column1 = value1, column2 = value2,...  WHERE condition;

**If we omit the WHERE clause from the update query then all of the rows will get updated** <br>
UPDATE Student SET NAME = ‘new_name’;

## DCL COMMANDS

As database security administrator, we use **Data Control Language** (DCL) SQL commands **to control user access to database objects and their contents**.

Security starts with the admin user. As the admin user, you must create and authorise other users. When you first create users, they cannot see or do anything. As you grant users more privileges, they can access more database objects.

When you create users, by default they have access only to system views. With these views, they can retrieve lists of user database objects and select data within those objects. Because security is also built into these system views, the list of database objects a user can see depends on the security privileges of the user.

DCL includes commands such as GRANT and REVOKE which mainly **deal with the rights, permissions, and other controls of the database system**. 

**GRANT** <br>
This command gives users access privileges to the database.

**REVOKE** <br>
This command withdraws the user’s access privileges given by using the GRANT command.

### Queries for DCL Commands

**Granting SELECT Privilege to a User in a Table** <br>
GRANT SELECT ON Users TO'user1'@'localhost;

**Granting more than one Privilege to a User in a Table** <br>
GRANT SELECT, INSERT, DELETE, UPDATE ON Users TO 'user1'@'localhost;

**Granting All the Privilege to a User in a Table** <br>
GRANT ALL ON Users TO 'user1'@'localhost;

**Granting a Privilege to all Users in a Table** <br>
GRANT SELECT  ON Users TO '*'@'localhost;

**execute a function or procedure** <br>
GRANT EXECUTE ON [ PROCEDURE | FUNCTION ] object TO user; 

**Granting EXECUTE privileges to all Users on a function in MySQL** <br>
GRANT EXECUTE ON [ PROCEDURE | FUNCTION ] TO '*'@localhost';

**view privileges granted to the user** <br>
SHOW GRANTS FOR  'Amit'@localhost';

**revoke some or all of the privileges which have been granted to a user in the past** <br>
REVOKE privileges ON object FROM user;

**Revoking SELECT Privilege to a User in a Table** <br>
REVOKE SELECT ON  users FROM 'Amit'@localhost'; 

**Revoking All the Privilege to a User in a Table** <br>
REVOKE ALL ON Users FROM 'Amit'@'localhost; 

**Revoking a Privilege to all Users in a Table** <br>
REVOKE SELECT  ON Users FROM '*'@'localhost; 

**Revoking Privileges on Functions/Procedures** <br>
REVOKE EXECUTE ON [ PROCEDURE | FUNCTION ] object FROM user;



