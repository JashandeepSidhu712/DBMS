# KEYS IN DBMS

In a database management system (DBMS), keys are attributes or sets of **attributes used to uniquely identify individual records (rows) in a table**. They play a critical role in establishing relationships between tables and ensuring data integrity.

## 1. SUPER KEY
In a database management system (DBMS), a super key is a **set of one or more attributes (columns) that can be used to uniquely identify individual records (rows) in a table**. 

1. A super key contains more attributes than the minimum required to achieve uniqueness, making the super key redundant.
2. It serves as a broader category of keys that can uniquely identify rows, including candidate keys and other combinations of attributes.

Example: <br>
Consider a table named "Student" <br>
![image](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/4f579eff-813a-4314-9801-a43247a01bbd) <br>
Consider different super keys
1. (StudentID): <br>
super key since it uniquely identifies each student. It contains the minimum number of attributes required for uniqueness, making it a candidate key.<br>
2. (StudentID, Email): <br>
super key since these together uniquely identifies each student, however, it contains more attributes than necessary for uniqueness, making it a composite key. <br>
3. (StudentID, FirstName, LastName): <br>
super key since these together uniquely identifies each student, however, it is redundant since "StudentID" alone already serves as a candidate key. <br>
4. (FirstName, LastName): <br>
super key since these together can uniquely identify students in this table, however, it is also redundant since "StudentID" alone already serves as a candidate key. <br>
5. (Phone): <br>
super key since the "Phone" column alone can uniquely identify students who have unique email addresses. However, it is not a candidate key because it allows NULL values.

## 2. CANDIDATE KEY
In a database management system (DBMS), a candidate key is a **minimal super key that uniquely identifies each record (row) in a table**.

1. It is a specific type of **super key that contains the minimum number of attributes (columns) required to achieve uniqueness**.
2. A candidate key is a super key with no unnecessary attributes, and it guarantees that no two rows in the table have the same combination of values in the candidate key columns.
3. **Each attribute in the candidate key is necessary for uniqueness** and cannot be removed without losing the uniqueness property, **does not have any redundant attributes**.
4. From all the candidate keys in a table, **one is selected to be the primary key**, which means it will be used as the main unique identifier for the table.

Example: <br>
Consider a table named "Employees" <br>
![image](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/56e9ef25-6f3c-4963-bc61-410d4ef45a7c) <br>
 "EmployeeID" column is a candidate key because it uniquely identifies each employee, and removing it would result in non-uniqueness.

## 3. PRIMARY KEY
The primary key is a **unique identifier for each record in a table**. 

1. It uniquely identifies each row.
2. No two rows can have the same primary key value. 
3. The **primary key column cannot have NULL values**.
4. A primary key can be referenced by other tables using foreign keys, establishing relationships between tables maintaining referential integrity.
5. It ensures that the table contains **only unique and valid data, preventing duplicate or inconsistent records.**

Example: <br>
Consider a table named "Student" <br>
![image](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/494775d3-10e5-499c-99ba-9e0c4d258404)
"StudentID" column uniquely identifies each student record and allows easy access to individual students' data.

## 4. ALTERNATE KEY
In a database management system (DBMS), an alternate key is a **candidate key that is not selected as the primary key for a table**.

1. Among the candidate keys, one is chosen as the primary key, and the **remaining candidate keys** are referred to as alternate keys.
2. An alternate key ensures that the combination of attributes it contains is unique for each record in the table.
3. It contains the **minimum number of attributes required for uniqueness but is not chosen as the primary key**.

Example: <br>
Consider a table named "Customers" <br>
![image](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/6f618d29-3957-4809-9a99-029d9fc4f9e1) <br>
"CustomerID" is the primary key and is used as the main identifier for each customer record. Both "Email" and "Phone" are alternate keys, each providing an alternative way to uniquely identify customers.


## 5. UNIQUE KEY
A unique key ensures that the **values in the specified column(s) are unique and do not have any duplicates**.

1.  It ensures that **no two rows in the table can have the same combination of values in the unique key column(s)**.
2.  A **unique key allows NULL values**.

Example: <br>
Consider a table named "Books". <br>
![image](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/559b848d-a254-4bbb-8ed6-d7b382141dd8) <br>
 "ISBN" column is a unique key, ensuring that each book in the "Books" table has a unique ISBN value, while allowing for NULL values if the ISBN is not provided.

 ## 6. COMPOSITE KEY
A composite key is a key that consists of **two or more attributes, working together to uniquely identify a row in a table**. 

1. Each individual attribute may not be unique, but the **combination of all the attributes in the composite key must be unique across all rows** in the table.
2. A composite key uses a combination of multiple columns to achieve uniqueness.
3. No two rows can have the same set of values in all the attributes that make up the composite key.
4. A **composite key doesnot allow NULL values**, all attributes in the composite key must have valid (non-NULL) values for each record.

Example: <br>
Consider a table named "Orders".
![image](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/719d683d-bb9a-4f27-b74d-b3abab0dd507) <br>
The combination of "CustomerID," "ProductID," and "OrderDate" forms a composite key, ensuring uniqueness for each order.

## 7. FOREIGN KEY
A foreign key is a **column or set of columns in one table that references the primary key of another table**. It establishes relationships between tables, enforcing **referential integrity**.

1. The foreign key in one table is used **to link or connect the data in that table to the data in another table**.
2. The data in the referencing table must correspond to valid data in the referenced table.

Example: <br>
Consider two tables, "Orders" and "Customers," <br>
![image](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/4b0af566-4928-45ae-b641-f72c89e98f4d) <br>
![image](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/4ba9463d-73a9-4c6e-aa68-6259e0c09a26) <br>
"CustomerID" in the "Orders" table acts as a foreign key, linking each order to the corresponding customer in the "Customers" table. The foreign key ensures that every "CustomerID" in the "Orders" table matches an existing "CustomerID" in the "Customers" table.





  ## CONSTRAINTS
Constraints are **rules or conditions applied to the data in a database table to maintain data integrity and ensure data consistency**. Constraints are used to enforce business rules and prevent the insertion of invalid or inconsistent data. 

