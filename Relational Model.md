# RELATIONAL MODEL

## RELATION/TABLE
A relation is a **two-dimensional table that represents data** in the database. It consists of **rows (tuples) and columns (attributes)**.  <br>
Each row in a relation represents a specific record or data entry, while each column represents an attribute or field that holds a specific type of data. <br>

```
+-------------+-------+-----+
| EmployeeID  | Name  | Age |
+-------------+-------+-----+
| 1           | John  | 30  |
| 2           | Mary  | 25  |
| 3           | Mike  | 40  |
+-------------+-------+-----+
```


## TUPLE/ROW
A tuple is a **single record or row** in a relation. It contains a **collection of attribute values**, where each attribute value corresponds to a specific column in the relation.

```
+-------------+-------+-----+
| EmployeeID  | Name  | Age |
+-------------+-------+-----+
| 1           | John  | 30  |
+-------------+-------+-----+
```

## ATTRIBUTE/COLUMN
An attribute is a **named data item** that **represents a characteristic or property of the entities** represented by the relation. Each attribute has a specific data type and domain, **defining the type of data it can hold**.

```
+-------------+
| EmployeeID  |
+-------------+
| 1           |
| 2           |
| 3           |
+-------------+
```

## DOMAIL
The domain is the **set of allowable values** for an attribute. It defines the **range of valid data** that can be stored in a particular attribute.

```
+---------------------------+
|     Domain: Age           |
+---------------------------+
| Valid Values: 0 to 150    |
+---------------------------+
```

## DEGREE OF THE TABLE
In the context of the relational model in database management systems (DBMS), the degree of a table refers to the **number of attributes (columns) in the table**. It represents the **total count of column**s present in a specific relation.

## RELATION SCHEMA
A relation schema, also known as a table schema, **defines the structure of a relation (table) in a relational database**. It describes the attributes (columns) that make up the table and specifies the data types and constraints associated with each attribute. The relation schema does not contain any actual data; it is a **blueprint for creating the table and organizing the data within it**.

**Components of Relation Schema**
1. Relation Name
2. Attributes (Columns)
3. Data Types
4. Domain Constraints
5. Key Constraints
6. Foreign Key Constraints

```
Relation Name: Employees
-----------------------------------
| Attribute     | Data Type       |
-----------------------------------
| EmployeeID    | Integer         |
| Name          | String(50)      |
| Age           | Integer         |
| Department    | String(100)     |
-----------------------------------
Key Constraints:
Primary Key: EmployeeID
```

## RELATION AS SUBSET OF CARTESIAN PRODUCT
The **Cartesian product combines all possible combinations of elements from each set**, and the **relation is then defined as a subset of this Cartesian product that includes only the valid combinations of attribute values**.

Let's illustrate this with a simple example. <br>
Consider a relation called "Students," with two attributes: "StudentID" and "Course." <br>
The sets representing the domains for each attribute are as follows: <br>
Set of StudentIDs: {101, 102, 103}
Set of Courses: {"Math", "Science", "History"}

The Cartesian product of these sets will contain all possible combinations: <br>
```
Cartesian Product of StudentIDs and Courses:
----------------------------------------------
| StudentID | Course                     |
----------------------------------------------
| 101       | "Math"                     |
| 101       | "Science"                  |
| 101       | "History"                  |
| 102       | "Math"                     |
| 102       | "Science"                  |
| 102       | "History"                  |
| 103       | "Math"                     |
| 103       | "Science"                  |
| 103       | "History"                  |
----------------------------------------------
```
Now, the relation "Students" will be a subset of this Cartesian product, including only specific valid combinations. Let's assume the relation "Students" contains the following tuples (rows):
```
Relation: Students
----------------------------------------------
| StudentID | Course                     |
----------------------------------------------
| 101       | "Math"                     |
| 102       | "Science"                  |
| 103       | "History"                  |
----------------------------------------------
```

## CARDINALITY IN RELATIONAL DATABASE MODEL
Cardinality refers to the **number of entities or rows in a relationship between two tables**. 

It describes the association or **mapping between the records of one table (parent table) and the records of another table (child table)** through a **common attribute**, which is **usually a foreign key**.

### 1. ONE-TO-ONE CARDINALITY (1:1)
In a one-to-one relationship, **each record in the parent table is associated with exactly one record in the child table**, and vice versa. <br>
This means that for each row in the parent table, there is a **unique** corresponding row in the child table, and no two rows in either table are related to the same row in the other table.

```
Table: Employee                                 Table: EmployeeContact
-------------------------------               -------------------------------
| EmployeeID (Primary Key)    |               | EmployeeID (Foreign Key)    |
-------------------------------               -------------------------------
| 101                         |               | 101                         |
| 102                         |               | 102                         |
| 103                         |               | 103                         |
-------------------------------               -------------------------------
```
![121](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/9d1e95de-4d53-46be-91dd-43553e748a0a) <br>
![onetoone](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/c6d35cb6-80cc-49f2-9627-80c7e85cb758)

### ONE-TO-MANY CARDINALITYT
In a one-to-many relationship, **each record in the parent table can be associated with multiple records in the child table**, but **each record in the child table can be associated with only one record in the parent table**. 

This means that one row in the parent table relates to many rows in the child table.

```
Table: Department                              Table: Employee
-------------------------------               +--------------------------------------------------------+
| DepartmentID (Primary Key)  |               | EmployeeID (Primary Key)  | DepartmentID (Foreign Key) |
-------------------------------               +--------------------------------------------------------+
| 1                           |               | 101                       | 1                          |
| 2                           |               | 102                       | 1                          |
-------------------------------               | 103                       | 2                          |
                                              +--------------------------------------------------------+
```

![12n](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/df950166-4a0a-458e-9b2f-5adb7e272f12) <br>
![onetomany](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/e206489c-4ad3-4aed-8459-59fc57cdec12)

### MANY-TO-MANY CARDINALITY
In a many-to-many relationship, **each record in the parent table can be associated with multiple records in the child table**, and vice versa. 

This is achieved through the use of an intermediate or junction table that contains the foreign keys of both tables, creating an indirect relationship.

```
Table: Student                                Table: Course
-------------------------------              -------------------------------
| StudentID (Primary Key)     |              | CourseID (Primary Key)      |
-------------------------------              -------------------------------
| 1                           |              | 101                         |
| 2                           |              | 102                         |
-------------------------------              -------------------------------

Junction Table: Enrollment
------------------------------------------------------
| StudentID (Foreign Key)   | CourseID (Foreign Key) |
------------------------------------------------------
| 1                         | 101                    |
| 1                         | 102                    |
| 2                         | 102                    |
------------------------------------------------------
```

![manytomantrelationship](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/f9f9cc32-491e-4c99-ad7e-2cb152c10f26) 

![manytomany](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/b444a03c-e8cc-4346-90ba-0c8d2b60126f)











