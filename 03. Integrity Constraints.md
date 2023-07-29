# INTEGRITY CONSTRAINTS

In a Database Management System (DBMS), integrity constraints are **rules or conditions that must be satisfied by the data in a database**. These constraints are defined to **ensure that the data remains consistent, accurate, and reliable**. They prevent invalid or inappropriate data from being entered into the database and help **maintain data integrity**.

## ENTITY INTEGRITY CONSTRAINTS:
This constraint ensures that the primary key attribute of a table is unique and cannot contain null values. It guarantees that each record in the table can be uniquely identified.

## REFERNTIAL INTEGRITY CONSTRAINTS:
This constraint maintains the consistency between relationships in different tables. It ensures that foreign key values in a table match the primary key values in another related table or are null. This way, it prevents orphaned or invalid references between tables.

## DOMAIN INTEGRITY CONSTRAINTS:
The domain integrity constraint ensures that the data entered in a column of a table satisfies the defined data type and format for that column. For example, a date column should only contain valid dates, and numeric columns should only contain numbers.

## KEY INTEGRITY CONSTRAINTS:
Key constraints define rules for the uniqueness of values within a column or set of columns. Besides the primary key constraint, there are unique key constraints that ensure the values in the specified column(s) are unique but allow null values.

## CHECK INTEGRITY CONSTRAINTS:
Check constraints impose specific conditions on the values that can be entered into a column. These conditions are defined using expressions or logical statements, and data that does not satisfy the condition will be rejected.

## DEFAULT INTEGRITY CONSTRAINTS:
Default constraints specify a default value for a column when a new record is inserted, provided no other value is specified explicitly for that column.

## SUMMARY

![image](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/0cdd3642-1f62-42e5-b26b-89a437a9f1e9)
