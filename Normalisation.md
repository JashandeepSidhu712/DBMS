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



 
