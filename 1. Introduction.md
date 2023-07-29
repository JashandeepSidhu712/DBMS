# DBMS INTRODUCTION

## DATA

**DEFINATION:** &nbsp; Data is a **collection of raw, unorganized facts and details** like text, observations, figures, symbols, and descriptions of things etc. In other words, data does not carry any specific purpose and has no significance by itself.  

**CHARACTERISTICS:** &nbsp; Data is typically in its most basic form, lacking any context or interpretation. It consists of individual data points that may not have immediate significance on their own.  <br>

**In a database, data is organized and stored in a structured manner**, making it easier to manage, retrieve, and manipulate. 	<br>
**Data is measured in terms of bits and bytes** – which are basic units of information in the context of computer storage and processing. 	<br>
Data can be recorded and doesn’t have any meaning unless processed. <br>

**EXAMPLE:** &nbsp; In a customer database, data could include individual entries with attributes like customer names, addresses, phone numbers, and purchase history. 

## INFORMATION

**DEFINATION:** &nbsp; Information is the **meaningful interpretation of data**. It is derived from the data through analysis, processing, and organization, providing valuable insights or answers to specific questions. <br>

**CHARACTERISTICS:** &nbsp; Information involves **processing and transforming data to make it relevant, valuable, and useful for decision-making**. It provides context and understanding to the data, enabling users to draw conclusions or take action. <br>

**EXAMPLE:** &nbsp; Information derived from the customer database could include reports on customer demographics, purchasing patterns, and total revenue generated during a specific period. <br>


## TYPES OF DATA

### 1. QUALITATIVE

**DEFINATION:** &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; Qualitative data consists of non-numeric attributes or characteristics that describe qualities or categories.	<br>
**REPRESENTATION:** &nbsp;&nbsp; It is descriptive in nature and cannot be measured on a numerical scale. <br> 
**EXAMPLES:** &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Qualitative data includes attributes such as names, colors, gender, country of origin, product categories, etc.<Br>
**DATA TYPE:** &nbsp; &nbsp; &nbsp;&nbsp;&nbsp; Qualitative data is categorized as nominal or ordinal data in terms of its classification.	

Nominal data represents categories with no inherent order, while ordinal data represents categories with a meaningful ranking or order. 	<br>
Nominal data is used for classification purposes where items are placed into distinct groups. 	<br>
Ordinal data is used when there is a meaningful order, but the actual differences between categories may not be precisely measurable or consistent.

### 2. QUANTATIVE

**DEFINATION:** &nbsp; &nbsp;&nbsp;&nbsp; &nbsp; Quantitative data consists of numerical values that represent measurable quantities or variables. 	<br>
**REPRESENTATION:** &nbsp; &nbsp; It can be measured on a numerical scale, allowing for mathematical operations and statistical analysis. 	<br>
**EXAMPLES:** &nbsp; &nbsp;&nbsp;&nbsp; &nbsp; &nbsp; Quantitative data includes attributes such as age, weight, temperature, number of items sold, income, etc. 	<br>
**DATA TYPE:** &nbsp; &nbsp;&nbsp;&nbsp; &nbsp; Quantitative data can be further classified as discrete or continuous based on the nature of the values. 	<br>

Discrete data comprises distinct and separate values that are countable and typically represented by whole numbers. 	<br>
Continuous data comprises an infinite set of values within a range and is not limited to whole numbers, allowing for more precise and detailed measurements.

## DATABASE

In the context of Database Management Systems (DBMS), a database is a structured collection of data that is organized, stored, and managed in a way that allows for efficient retrieval, updating, and querying of information.

A database acts as a centralized repository to store large volumes of data, making it easier for users or applications to interact with the data in a structured and controlled manner.

## DATA WAREHOUSE

A Data Warehouse is a specialized type of database used in Database Management Systems (DBMS) that is designed to store and manage large volumes of historical and aggregated data from various sources within an organization. 

Its primary purpose is to support business intelligence (BI) and analytics activities, providing a consolidated view of data for decision-making and reporting.

## DATABASE MANAGEMENT SYSTEM

A Database Management System (DBMS) is a software application or system that facilitates the creation, organization, management, and manipulation of databases. 

It serves as an interface between users or applications and the underlying database, providing efficient and secure access to data. <br> The primary goal of a DBMS is to ensure data integrity, consistency, and efficiency in data storage and retrieval operations.

## DATABASE ADMINISTRATOR

A Database Administrator (DBA) is a professional responsible for the design, implementation, maintenance, and security of a database management system (DBMS) within an organization. <br>
DBAs play a crucial role in ensuring that the database infrastructure runs efficiently, securely, and meets the data management needs of the organization.

Functions of Database Administrator

**1. Database Design**: DBAs participate in the design phase of a database, helping to create the database schema, defining tables, columns, relationships, and data constraints to ensure data integrity. <br>
**2. Database Installation and Configuration**: DBAs are responsible for installing and configuring the DBMS software, setting up database instances, and managing system parameters for optimal performance. <br>
**3. Data Security**: DBAs implement security measures to protect sensitive data from unauthorized access. They manage user access rights, roles, and permissions to control data access. <br>
**4. Data Backup and Recovery**: DBAs design and implement backup and recovery strategies to ensure data can be restored in case of data loss, system failures, or disasters. <br>
**5. Database Performance Tuning**: DBAs monitor database performance, identify bottlenecks, and optimize queries, indexes, and database configurations for improved performance. <br>
**6. Database Maintenance**: DBAs perform routine maintenance tasks such as data archiving, index rebuilding, and database reorganization to keep the database running smoothly. <br>
**7. Database Monitoring**: DBAs continuously monitor the database for issues, errors, and performance metrics to proactively address potential problems. <br>
**8. Database Upgrades and Patches**: DBAs manage database upgrades and apply patches to ensure the DBMS is running with the latest features and security fixes. <br>
**9. Data Migration**: DBAs plan and execute data migrations between different database systems or versions, ensuring data integrity during the process.<br>
**10. Database Documentation**: DBAs maintain documentation related to the database design, configurations, and procedures for reference and compliance. <br>

Database Administrators work closely with developers, system administrators, and business stakeholders to ensure that the database meets the organization's needs and supports its applications effectively. 

## HOW IS DATABASE ACCESSED FROM APPLICATION PROGRAMS?

**Database Connectivity APIs** <br>
DBMS vendors provide Database Connectivity APIs that allow application programs to interact with the database using standard programming languages. <br>
The most widely used API is the ODBC (Open Database Connectivity) for relational databases, which provides a vendor-neutral way to access various DBMSs. Other common APIs include JDBC (Java Database Connectivity) for Java applications and ADO.NET for .NET applications.

**Embedded SQL or SQL APIs** <br>
Embedded SQL allows SQL statements to be directly embedded within the application code. The application program contains SQL queries or statements written in the programming language (e.g., C, C++, COBOL, etc.), and these queries are preprocessed and executed by the DBMS during runtime. This approach is especially common in legacy applications and systems.

**Steps involved in accessing a database from an application program** are as follows: <br>
1. Establishing a Connection
2. Sending SQL Queries
3. Query Execution
4. Handling Results
5. Closing the Connection

