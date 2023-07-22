# KEYS IN DBMS

In a database management system (DBMS), keys are attributes or sets of **attributes used to uniquely identify individual records (rows) in a table**. They play a critical role in establishing relationships between tables and ensuring data integrity.


## 1. PRIMARY KEY
The primary key is a **unique identifier for each record in a table**. 

1. It uniquely identifies each row.
2. No two rows can have the same primary key value. 
3. The primary key column cannot have NULL values.
4. A primary key can be referenced by other tables using foreign keys, establishing relationships between tables maintaining referential integrity.
5. It ensures that the table contains only unique and valid data, preventing duplicate or inconsistent records.

Example: <br>
Consider a table named "Student" <br>
![image](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/494775d3-10e5-499c-99ba-9e0c4d258404)
"StudentID" column uniquely identifies each student record and allows easy access to individual students' data.

## 2. UNIQUE KEY
A unique key ensures that the **values in the specified column(s) are unique and do not have any duplicates**.

1.  It ensures that no two rows in the table can have the same combination of values in the unique key column(s).
2.  A unique key allows NULL values.

Example: <br>
Consider a table named "Books". <br>
![image](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/559b848d-a254-4bbb-8ed6-d7b382141dd8)
 "ISBN" column is a unique key, ensuring that each book in the "Books" table has a unique ISBN value, while allowing for NULL values if the ISBN is not provided.


  ## CONSTRAINTS
Constraints are **rules or conditions applied to the data in a database table to maintain data integrity and ensure data consistency**. Constraints are used to enforce business rules and prevent the insertion of invalid or inconsistent data. 

