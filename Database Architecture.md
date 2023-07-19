## THREE SCHEMA ARCITECTURE

The Three Schema Architecture, also known as the ANSI/SPARC architecture, is a conceptual framework that defines the three levels of abstraction in a Database Management System (DBMS). <br>
It provides a clear separation between the **user view, logical view, and physical view of the database**.

The major purpose of DBMS is to provide users with an **abstract view** of the data. That is, the system hides certain details of how the data is stored and maintained. <br>
To simplify user interaction with the system, abstraction is applied through several levels of abstraction.

The main objective of three level architecture is to **enable multiple users to access the same data with a personalized view** while storing the underlying data only once

The Three Schema Architecture separates the concerns of data representation, logical organization, and physical storage, enabling flexibility, modularity, and data independence. <br>
It allows for **changes or modifications at one level without impacting other levels**. This architecture facilitates data abstraction, security, scalability, and maintainability in complex database systems.

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

