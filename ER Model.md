# ENTITY-RELATIONSHIP MODEL

The Entity-Relationship (ER) model is a conceptual data model used in database management systems (DBMS) to **represent the structure and relationships between entities in a database**.

The ER model is widely used in database design and serves as a basis for **converting conceptual data requirements into a logical database schema**. <br>
The ER model is typically visualized using ER diagrams, which are **graphical representations** of the entities, attributes, and relationships. 

The ER model aims to **represent real-world entities and their relationships in a database**. As such, the process of designing an ER model often involves close collaboration with domain experts to understand the semantics and constraints of the data being represented.

The ER model provides a **high-level representation of data requirements**. During database design, the **ER model is typically transformed into a logical schema**, such as the relational model, which uses tables, keys, and foreign keys **to represent entities and relationships** in a DBMS.

## ENTITY
Entities represent **real-world objects or concepts that we want to store information about in the database**.

Entities are the core building blocks of a database and are **used to organize and classify data**. Each entity corresponds to a table in the relational database model, where each row in the table represents a specific instance or occurrence of that entity.

**STRONG ENTITY**<br>
A strong entity is an entity that exists independently and has its attributes. It can be identified uniquely without relying on other entities.

**WEAK ENTITY** <br>
A weak entity is an entity that cannot be uniquely identified without the help of another related entity. It depends on a strong entity for its existence. Weak entities have a partial key that, along with the key of the related strong entity, forms a unique identifier.

**ASSOCIATIVITY ENTITY** <br>
Also known as a "Bridge Entity" or "Junction Entity," an associative entity is used to represent a many-to-many relationship between two other entities. It contains attributes that are specific to the relationship between the two entities.

## ENTITY SET
An entity set is a **collection of similar entities that share the same attributes**. It represents a **logical grouping of entities based on common characteristics**. An entity set is the set of all instances (individual occurrences) of a particular entity type.

The entity sets allow us to organize and manage the data efficiently, making it easier to represent the relationships between books and authors in the library database.

## ATTRIBUTES
An attribute is a fundamental building block used to **describe the properties or characteristics of an entity**. 

An attribute represents a specific piece of data associated with an entity and **provides information about that entity**. In other words, it defines what kind of data can be stored for each instance of the entity.


