# NORMALISATION

Normalization is a systematic approach used to organize and structure data in such a way that it **reduces redundancy**, **minimizes data anomalies**, and **ensures data integrity**. 
 
The primary goal of normalization is to **design a database schema that avoids data duplication and maintains data consistency**, making it **easier to update, insert, and retrieve data without introducing inconsistencies**.

Normalization is not primarily used for optimization, but rather for **data organization, integrity, and consistency**. <br>
The main objectives of normalization are to eliminate data redundancy and anomalies, maintain data integrity, and improve data integrity. 

While these objectives indirectly contribute to better performance, the primary goal is to design a well-structured database that accurately represents the real-world entities and their relationships.

## ISSUES CAUSED BY REDUNDANT DATA

1. Data Inconsistency
2. Increased Storage Space
3. Update Anomalies
4. Insertion Anomalies
5. Deletion Anomalies
6. Performance Issues

## ANAMOLIES
Anomaly refers to **unexpected or undesirable behaviors** that can **occur when performing operations like insert, update, or delete** due to the way data is organized or structured. 

Anomalies are typically associated with **poorly designed or non-normalized databases**.

**Insertion anomaly** <br>
When certain data (attribute) can not be inserted into the DB without the presence of other data.

**Deletion anomaly** <br>
The delete anomaly refers to the situation where the deletion of data results in the unintended loss of some other important data.

**Updation anomaly** <br>
The update anomaly is when an update of a single data value requires multiple rows of data to be updated.

## TYPES OF NORMALISATION

**First Normal Form (1NF)** <br>
Eliminate duplicate rows in a table. <br>
Ensure each column contains only atomic values (no multi-valued attributes). <br>
Introduce a primary key to uniquely identify each row. <br>

**Second Normal Form (2NF)** <br>
Meet all the requirements of 1NF. <br>
Remove partial dependencies, ensuring non-key attributes are fully dependent on the entire primary key. <br>

**Third Normal Form (3NF)** <br>
Satisfy all the conditions of 2NF. <br>
Eliminate transitive dependencies, ensuring non-key attributes depend only on the primary key and not on other non-key attributes. <br>

**Boyce-Codd Normal Form (BCNF)** <br>
Meet all the conditions of 3NF. <br>
Ensure that every determinant (attribute that determines other attributes) is a candidate key. In other words, there should be no non-trivial functional dependencies on attributes that are not part of a candidate key. <br>

**Fourth Normal Form (4NF)** <br>
Satisfy all the requirements of BCNF. <br>
Remove multi-valued dependencies between attributes, ensuring that each multi-valued attribute is stored in a separate table. <br>

**Fifth Normal Form (5NF) or Project-Join Normal Form (PJNF)** <br>
Meet all the conditions of 4NF. <br>
Eliminate join dependencies, ensuring that all join dependencies are implied by candidate keys. <br>


## EXAMPLE TABLE

![image](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/bb64c846-70dc-4773-bc6d-aebf2f7e0ccf)

## FIRST NORMAL FORM
"Skills" column contains multiple values separated by commas, which violates the 1NF requirement of atomic values.

To convert this table to 1NF, we need to split the multi-valued attribute into separate rows and introduce a primary key for uniqueness.

![image](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/e7ecb740-ca4c-4b57-826a-a4df7484a2da)

## SECOND NORMAL FORM
To be in the Second Normal Form (2NF), a table must first be in 1NF and must eliminate partial dependencies. Partial dependencies occur when an attribute depends on only a part of the primary key.

In the current table, we have a composite primary key consisting of both Employee ID and Skill since Employee ID can be repeated, but the combination of Employee ID and Skill makes each row unique.

However, we can see that the attribute "Employee Name" depends only on "Employee ID" and not on the entire composite primary key. This is a partial dependency and violates the Second Normal Form (2NF).

To convert this table to 2NF, we split it into two separate tables: one for employee information and another for skills. We use a **foreign key** to establish a relationship between the tables.

![image](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/4addb738-eaf7-4225-92bb-e22f8da5d6b6)

The Employee ID serves as the primary key in the Employee table and is used as a foreign key in the Skill table to establish the relationship between the two. By doing so, we have eliminated the partial dependency and achieved the Second Normal Form (2NF).

## THIRD NORMAL FORM
To be in the Third Normal Form (3NF), a table must first be in 2NF and eliminate transitive dependencies. Transitive dependencies occur when an attribute depends on another non-key attribute rather than directly on the primary key.

In the current table, we can see that "Employee Name" depends only on the "Employee ID," which is the primary key. However, there is also a dependency between "Skill" and "Employee Name." "Skill" depends on "Employee ID," and "Employee Name" depends on "Employee ID," which creates a transitive dependency.

To convert this table to 3NF, we further split it into three separate tables: one for employee information, one for skills, and one for the relationship between skills and employees. We use foreign keys to establish the relationships.

![image](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/1befa5aa-fda7-4c97-95dd-90ccb19a8a26)

![image](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/08bd0c7d-3000-4850-9c21-5c880e860cf9)

![image](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/dda383aa-8a4d-4660-9eb2-fb8ab8386610)

The Employee ID is the primary key in the Employee table, the Skill ID is the primary key in the Skill table, and the Employee ID and Skill ID together form the composite primary key in the Employee-Skill Relationship table. By doing this, we have eliminated the transitive dependency and achieved the Third Normal Form (3NF).

## BOYCE CODD NORMAL FORM
To be in Boyce-Codd Normal Form (BCNF), a table must first be in 3NF and satisfy an additional requirement related to functional dependencies.

In the current table, all functional dependencies are satisfied, and there are no partial or transitive dependencies. Therefore, the table is in the Third Normal Form (3NF).

To convert this table to Boyce-Codd Normal Form (BCNF), we examine the functional dependencies and ensure that every determinant is a candidate key.

Functional Dependencies: <br>
Employee ID → Employee Name (Candidate Key: Employee ID)
Skill ID → Skill (Candidate Key: Skill ID)

Since all the functional dependencies have candidate keys as determinants, the table is already in Boyce-Codd Normal Form (BCNF). It satisfies the requirements of 3NF and has no non-trivial functional dependencies on attributes that are not part of the candidate keys. Hence, it is in BCNF.

## FOURTH NORMAL FORM
To be in the Fourth Normal Form (4NF), a table must first be in BCNF and eliminate multi-valued dependencies.

In the current table, there are multi-valued dependencies between Employee ID and Skill ID, as each employee can have multiple skills, and each skill can be associated with multiple employees.

To convert this table to Fourth Normal Form (4NF), we split the table into two separate tables, one for employee skills and another for skill employees. We use primary keys and foreign keys to establish relationships.

![image](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/db633c34-0661-48bd-b2c8-7bd80d7563fc)

![image](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/f4d957b7-e3b3-483b-90df-ef8fba0c4c59)

Now, we have two separate tables with no multi-valued dependencies. Each table represents a distinct relationship, and each attribute depends on the primary key of its respective table.

## FIFTH NORMAL FORM
To achieve the Fifth Normal Form (5NF) for a table, it must first be in Fourth Normal Form (4NF) and eliminate join dependencies.

In the current tables, there are join dependencies between Employee-Skill Table and Skill-Employee Table. To be in Fifth Normal Form (5NF), we split the tables even further and create three separate tables: Employee Table, Skill Table, and Employee-Skill Relationship Table.

![image](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/d619148f-025b-4947-aec2-2ff73b940510)

![image](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/4d1a05cc-c67e-4968-9fe6-4886904728d5)

![image](https://github.com/JashandeepSidhu712/DBMS/assets/117754690/529ebc32-9f8f-4620-bd1a-ea0b2ac81961)

Now, each table contains a distinct set of information, and there are no join dependencies between them. Each table represents a single entity and maintains data integrity without redundant data or functional dependencies.

## PERFORMANCE IMPLICATION OF NORMALISATION

**Data Retrieval Efficiency** <br>
Highly normalized databases reduce data redundancy by breaking data into multiple related tables. <br>
This is beneficial for data integrity and consistency. However, when retrieving data from such databases, it often requires joining multiple tables together. <br>
Joining tables can be computationally expensive and can potentially slow down data retrieval operations, especially in complex queries. <br>
So, the optimization challenge is to strike a balance between reducing data redundancy (through normalization) and simplifying data retrieval operations for better performance. <br>
Sometimes, for performance-critical situations, denormalization (introducing controlled redundancy) might be considered to simplify queries and improve data retrieval efficiency. <br>
However, denormalization needs to be done carefully to maintain data integrity and avoid potential data anomalies. <br>

**Insert, Update, and Delete Operations** <br>
Highly normalized databases may require more complex operations when inserting, updating, or deleting records due to the need to maintain referential integrity across related tables. <br>
This can impact the performance of write operations.

**Disk Space Utilization** <br>
Normalization can help reduce data duplication, which can lead to a more efficient use of disk space. However, this advantage needs to be balanced with potential performance trade-offs.

**Data Integrity** <br>
By eliminating data redundancy and ensuring data dependencies are well-managed, normalization helps maintain data integrity. Inconsistent data can lead to errors and inefficiencies in the application.



 
