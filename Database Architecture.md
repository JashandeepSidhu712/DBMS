## INSTANCES

An instance of a database refers to the **actual data stored in the database at a specific point in time**. <br>
It represents the **current snapshot of the data that reflects the changes and updates made by users or applications**. 

When a DBMS is installed and running, it creates an instance of the database in memory, allowing users and applications to interact with the data in real-time. Any modifications to the data, such as inserts, updates, or deletes, are reflected in the database instance.

## SCHEMA

A schema in a DBMS defines the **logical structure and organization of the database**. It represents the **overall design of the database**, including the tables, columns, data types, constraints, and relationships between tables.

The schema acts as a blueprint for the database and serves as a **reference for how the data is structured and related**. It provides a consistent and standardized way to define and access data for all users and applications.

### Types of Schema

**External Schema (User View)**: &nbsp; Defines the user-specific view of the database, tailored to the requirements of individual users or applications. <br>
**Conceptual Schema (Logical View)**: &nbsp; Represents the overall logical view of the entire database, providing an integrated and neutral representation of the data. <br>
**Internal Schema (Physical View)**: &nbsp; Describes how data is physically stored and organized on the storage media, focusing on the implementation details. <br>

## THREE SCHEMA ARCITECTURE

The Three Schema Architecture, also known as the ANSI/SPARC architecture, is a conceptual framework that defines the three levels of abstraction in a Database Management System (DBMS). <br>
It provides a clear separation between the **user view, logical view, and physical view of the database**.

The major purpose of DBMS is to provide users with an **abstract view** of the data. That is, the system hides certain details of how the data is stored and maintained. <br>
To simplify user interaction with the system, abstraction is applied through several levels of abstraction.

The main objective of three level architecture is to **enable multiple users to access the same data with a personalized view** while storing the underlying data only once

It allows for **changes or modifications at one level without impacting other levels**. This architecture facilitates data abstraction, security, scalability, and maintainability, flexibility, modularity, and data independence in complex database systems.

                  +-----------------------+
                    ** External Schema **   
                  | (User View)           |
                  |                       |
                  |    User/Application   |
                  |     Specific View     |
                  +-----------------------+
                      **EXTERNAL LEVEL**
                             |
                             |
                             V
                  +-----------------------+
                  | **Conceptual Schema** |
                  | (Logical View)        |
                  |                       |
                  |    Integrated View    |
                  +-----------------------+
                    **CONCEPTUAL LEVEL**
                             |
                             |
                             V
                  +-----------------------+
                  | **Internal Schema**   |
                  | (Physical View)       |
                  |                       |
                  |    Physical Storage   |
                  +-----------------------+
                    **INTERNAL LEVEL**
                             |
                             |
                             V
                  +-----------------------+
                  | **Database**          |
                  |                       |
                  |                       |
                  |                       |
                  +-----------------------+

### Internal Level / Physical Level

Internal Level represents the lowest level of abstraction and corresponds to the physical view of the database. <br>
It describes how data is physically stored, organized, and accessed on the storage media, such as disks or memory, at a low-level technical implementation.

It provides a **mapping between the conceptual schema and the physical storage representation, translating the logical structure into the physical representation**.

### Conceptual Level / Logical Level

"Conceptual Level represents the middle layer of abstraction and **overall logical view of the entire database**, also known as the logical view. <br>
It focuses on providing an integrated and global representation of the entire database, independent of any specific user's view or physical storage considerations.

It describes the structure, relationships, and constraints of the data in a neutral and abstract manner.

It serves as a **bridge between the external schemas and the physical schema, ensuring data consistency and integrity** across different user views.

### External Level / User View Level

External Level also known as the User View, represents the highest level of abstraction and **corresponds to the individual user's or application's perspective of the database**. <br>
It focuses on defining specific views tailored to the requirements of each user or group of users.

It defines the user's access rights, views, and the logical organization of the data to facilitate efficient retrieval and manipulation.

