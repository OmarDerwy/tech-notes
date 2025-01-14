# 1	[[iti/Database/Revision|Revision]] 
## 1.1	Exploring SQL Join Types

While the sources primarily focus on database design principles like normalization and key types, they provide some context for understanding SQL joins within [1]. Joins are crucial for combining data from multiple tables based on relationships established through foreign keys, a concept discussed in our previous conversation. Let's explore different SQL join types:

### 1.1.1	Inner Join

- **Combines rows from two tables only when the join condition is met in both tables**.
- This results in a result set containing only matching rows based on the specified criteria.
- The sources illustrate this with an example involving "Customers" and "Stores" tables [1]. The goal is to identify customers and stores located in the same city. Using an inner join on the "City" column, the query returns rows where a matching city exists in both tables.
- Importantly, if a customer or store's city doesn't have a match in the other table, that row is excluded from the results.

### 1.1.2	Other Join Types

The sources briefly mention the existence of other join types beyond inner joins [1], classifying them into broader categories:

- **Outer Joins:** Designed to include rows even when there's no match in the other table. They come in three variations:
- **Left Outer Join:** Includes all rows from the left table and matching rows from the right table. If there's no match on the right, the result includes NULL values for the right table's columns.
- **Right Outer Join:** Mirrors the left outer join, including all rows from the right table and matching rows from the left.
- **Full Outer Join:** Combines the results of both left and right outer joins, including all rows from both tables and filling in NULL values where there are no matches.
- **Semi-Join and Anti-Join:** These are less common join types, often used for filtering data based on the existence or absence of a match in another table. However, the sources don't provide specific details about these types.

### 1.1.3	Importance of Joins

Understanding different join types is essential for writing effective SQL queries to extract meaningful insights from relational databases. The choice of join depends on the specific question being asked and the desired outcome.

**Note:** This explanation builds upon the limited information provided in the sources and incorporates general knowledge of SQL join types. You may want to consult additional SQL resources for more comprehensive explanations and examples of outer joins, semi-joins, and anti-joins.

## 1.2	Exploring Entity Relationships

The sources provide detailed information about various aspects of database design, particularly emphasizing the importance of **relationships between entities** in constructing a robust and efficient relational database. Let's outline the key types of entity relationships, drawing upon the information provided:

### 1.2.1	**1. Based on Degree (Number of Entity Types Involved)**

The sources highlight the concept of **degree**, which refers to the number of entity types participating in a relationship.

- **Unary Relationship (Degree 1):**
- Involves a relationship within a single entity type.
- The sources illustrate this with a social media platform where users can be friends with other users. The "friend" relationship connects entities of the same type – "User."
- **Binary Relationship (Degree 2):**
- The most common type, involving two entity types.
- Examples:
- An employee "works in" a department.
- A student "enrolls in" a course.
- **Ternary Relationship (Degree 3):**
- Involves three entity types.
- Example: The sources use a university setting – a "teaches" relationship connecting "Teacher," "Course," and "Student" entities. This relationship signifies that a particular teacher instructs a specific course to a designated student.
- **Higher-Degree Relationships:** While possible, relationships involving more than three entity types are less frequent. The sources don't provide specific examples of these.

### 1.2.2	**2. Based on Cardinality (Number of Entities Participating)**

The sources emphasize the importance of **cardinality**, which specifies how many instances of one entity can be associated with instances of another entity in a relationship. They present two primary aspects of cardinality:

- **Cardinality Ratio:** Expressed as "one-to-one" (1:1), "one-to-many" (1:M), or "many-to-many" (M:M). It describes the maximum number of entities on each side of the relationship.
- **Participation Constraint:** Indicates whether an entity's participation in a relationship is mandatory (total participation) or optional (partial participation).

To illustrate these concepts, the sources use various examples. Let's break them down:

**Example 1: Employee and Department**

- An employee can work in only one department at a time.
- A department can have many employees.
- **Cardinality Ratio:** 1:M (one-to-many) from Employee to Department.
- **Participation Constraint:**Total participation from Employee (every employee must belong to a department).
- Partial participation from Department (a department might not have any employees yet).

**Example 2: Order and Product**

- An order can contain multiple products.
- A product can be included in multiple orders.
- **Cardinality Ratio:** M:M (many-to-many)
- **Participation Constraint:**Total participation from Order (an order must have at least one product).
- Partial participation from Product (a product might not have been ordered yet).

The sources provide a visual representation of these relationships using Entity-Relationship Diagrams (ERDs), which employ symbols to depict cardinality ratios and participation constraints. They demonstrate two common notations:

- **Chen Notation:** Uses diamonds for relationships, connecting lines to represent cardinality ratios, and double lines for total participation.
- **Crow's Foot Notation:** Employs a "crow's foot" symbol to indicate the "many" side of a relationship.

### 1.2.3	Key Takeaways

- Understanding relationship types between entities is fundamental to database design.
- Degree and cardinality are crucial concepts for defining these relationships accurately.
- Choosing the appropriate relationship type influences data integrity, query efficiency, and the overall structure of the database.
- ERDs are valuable tools for visually representing and communicating these relationships.

The sources offer a thorough explanation of these concepts using relatable examples, facilitating a deeper understanding of how entities connect within a relational database.


## 1.3	Different Types of Database Keys

The sources discuss various types of database keys and their significance in relational database design. Here's a breakdown:

### 1.3.1	Super Keys

- A super key is **any combination of attributes (columns) that can uniquely identify a row in a table**. [1]
- Super keys can include unnecessary attributes. [2]
- The sources provide an example using an "Employees" table. In this example, possible super keys include:
- Social Security Number (SSN) alone (as it's assumed to be unique for each employee). [3]
- Email alone (as it's also assumed to be unique). [3]
- The combination of SSN and email. [4]
- Name, Department, and Email. [4]

### 1.3.2	Candidate Keys

- Candidate keys are a **subset of super keys**. [5, 6]
- They are **minimal super keys, meaning they contain only the necessary attributes for unique identification**. [7]
- Any unnecessary attributes are removed. [8]
- From the "Employees" table example, the candidate keys are:
- SSN
- Email

### 1.3.3	Primary Key

- The primary key is **the candidate key chosen to uniquely identify each row in a table**. [6, 9]
- Each table has only one primary key. [9]
- The primary key **cannot contain null values**. [10]
- It should be **stable and not change frequently**. [9, 10]

### 1.3.4	Alternate Key

- Alternate keys are **candidate keys that were not selected as the primary key**. [10]
- In the "Employees" example, if "Email" is chosen as the primary key, then "SSN" would be considered an alternate key.

### 1.3.5	Foreign Key

- Foreign keys are **attributes in one table that refer to the primary key of another table**. [11, 12]
- They **establish relationships between tables**. [12]
- Foreign keys help **maintain data integrity by preventing the insertion of values that don't exist in the referenced table**. [12, 13]
- For example, if an "Orders" table has a "CustomerID" column that references the "ID" column (primary key) of a "Customers" table, "CustomerID" would be a foreign key in the "Orders" table.

### 1.3.6	Natural Keys vs. Surrogate Keys

- **Natural keys** are attributes that have meaning outside the database, like SSN, email, or airport codes. [14, 15]
- **Surrogate keys** are artificial attributes created solely for database identification, typically integer values like an auto-incrementing "ID". [14]
- Using natural keys as primary keys can be convenient, but it's essential to ensure their stability and uniqueness. [15]
- Surrogate keys are useful when no suitable natural key exists. [16]

The sources emphasize the importance of carefully choosing primary and foreign keys to ensure data integrity and avoid anomalies in a relational database.

## 1.4	Subtypes of SQL Language with Examples

The sources focus on database design concepts, including normalization forms, ER diagrams, and database keys, but they don't explicitly discuss subtypes of SQL language. However, based on general knowledge, here are the subtypes of SQL language with short examples:

### 1.4.1	**1. Data Definition Language (DDL)**

DDL is used to define the structure of the database.

- **CREATE:** Creates new database objects such as tables, views, indexes, etc.
- Example: CREATE TABLE Employees (ID INT, Name VARCHAR(255), Salary DECIMAL);
- **ALTER:** Modifies existing database objects.
- Example: ALTER TABLE Employees ADD Department VARCHAR(255);
- **DROP:** Deletes existing database objects.
- Example: DROP TABLE Employees;
- **TRUNCATE:** Deletes data from a table while keeping the table structure intact.
- Example: TRUNCATE TABLE Employees;

### 1.4.2	**2. Data Manipulation Language (DML)**

DML is used to manipulate data within the database.

- **INSERT:** Adds new data into a table.
- Example: INSERT INTO Employees (ID, Name, Salary) VALUES (1, 'John Doe', 50000);
- **SELECT:** Retrieves data from a table.
- Example: SELECT * FROM Employees WHERE Department = 'Sales';
- **UPDATE:** Modifies existing data in a table.
- Example: UPDATE Employees SET Salary = 60000 WHERE ID = 1;
- **DELETE:** Removes data from a table.
- Example: DELETE FROM Employees WHERE ID = 1;

### 1.4.3	**3. Data Control Language (DCL)**

DCL is used to control access and permissions to the database.

- **GRANT:** Gives specific permissions to users.
- Example: GRANT SELECT, INSERT ON Employees TO User1;
- **REVOKE:** Removes permissions from users.
- Example: REVOKE UPDATE ON Employees FROM User1;

### 1.4.4	**4. Transaction Control Language (TCL)**

TCL is used to manage transactions within the database.

- **COMMIT:** Makes changes permanent in the database.
- Example: COMMIT;
- **ROLLBACK:** Undoes changes made to the database.
- Example: ROLLBACK;
- **SAVEPOINT:** Creates a point within a transaction to which you can rollback.
- Example: SAVEPOINT MySavepoint;

These subtypes work together to provide a comprehensive language for managing and interacting with relational databases.

Please note that this explanation and examples are based on general knowledge of SQL and are not derived from the provided sources.

## 1.5	Summary of the 5 Normalization Forms

The sources discuss database normalization, a process used to organize data effectively and minimize redundancy and inconsistencies. [1, 2] Normalization involves dividing larger tables into smaller ones to reduce data duplication and improve data integrity. [1-3] This is achieved through a series of steps called Normal Forms (NF). [4] Each NF builds upon the previous one, adding more rules to ensure better data organization. [4] The sources describe five normal forms, from 1NF to 5NF, and highlight the importance of achieving these forms to minimize data anomalies. [1, 2, 5]

Here's an outline of the five normal forms, with brief examples from the sources:

### 1.5.1	**First Normal Form (1NF)**

- **No multi-valued attributes:** Each column in a table should contain a single value. [6, 7]
- **No use of row order to represent data:** The order in which rows are stored should not imply any specific meaning. [7-9]
- **Primary Key:** Each table must have a primary key to uniquely identify each row and prevent duplicate rows. [7, 10]

For example, storing multiple team members in a single cell would violate 1NF. [6] Instead, each team member should have their own row in the table. [11]

### 1.5.2	**Second Normal Form (2NF)**

- **Must satisfy 1NF.** [7, 12]
- **Non-key attributes fully dependent on the primary key:** Every column that is not part of the primary key should depend on the entire primary key, not just a part of it. [12]

For example, in a table with student ID and course as the primary key, the instructor's name should depend only on the course, not the student ID. [12] This would require separating the instructor data into a different table. [13]

### 1.5.3	**Third Normal Form (3NF)**

- **Must satisfy 2NF.** [14]
- **No transitive dependency:** Non-key attributes should not depend on other non-key attributes. [15]

For example, in a table with course and instructor as the primary key, storing the instructor's phone number would violate 3NF, as it depends on the instructor, not directly on the course. [15] The phone number should be moved to a separate table with the instructor. [16]

### 1.5.4	**Boyce-Codd Normal Form (BCNF)**

- **Considered an enhanced version of 3NF.** [14]
- **No attribute should depend on a non-key attribute.** [14] This rule applies to all attributes, not just non-key attributes.

BCNF is stricter than 3NF, but in practice, most tables satisfying 3NF also satisfy BCNF. [17]

### 1.5.5	**Fourth Normal Form (4NF)**

- **Must satisfy 3NF (and typically BCNF).** [18]
- **No multi-valued dependencies:** A table should not have multiple multi-valued dependencies that are independent of each other. [19]

For example, if a clothing item's available colors and sizes are independent of each other, storing them in a single table would violate 4NF. [19] This issue can be resolved by separating the color and size information into different tables. [20]

### 1.5.6	**Fifth Normal Form (5NF)**

- **Must satisfy 4NF.** [18]
- **No join dependency:** A table should not be decomposable into smaller tables without losing information when joined back together. [18]

For example, a table representing customer preferences for pizza brands and flavors might violate 5NF if it can be split into separate tables for brands, customers, and flavors without losing information. [21, 22]

Normalization forms help create a well-structured database that minimizes redundancy and inconsistencies. [1, 2] By understanding and applying these forms, you can ensure the integrity and efficiency of your database design.

[[Summary|Summary]]