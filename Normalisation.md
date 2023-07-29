# NORMALISATION

 Normalization is a systematic approach used to organize and structure data in such a way that it **reduces redundancy**, **minimizes data anomalies**, and **ensures data integrity**. 
 
 The primary goal of normalization is to **design a database schema that avoids data duplication and maintains data consistency**, making it **easier to update, insert, and retrieve data without introducing inconsistencies**.

Normalization is not primarily used for optimization, but rather for **data organization, integrity, and consistency**. <br>
The main objectives of normalization are to eliminate data redundancy and anomalies, maintain data integrity, and improve data integrity. 

While these objectives indirectly contribute to better performance, the primary goal is to design a well-structured database that accurately represents the real-world entities and their relationships.

#







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



 
