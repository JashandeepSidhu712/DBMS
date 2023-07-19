# DATABASE LANGUAGES

## DDL COMMANDS

DDL or Data Definition Language actually consists of the SQL commands that can be used to define the database schema. <br>
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


### Queries

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
