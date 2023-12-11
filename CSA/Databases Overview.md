# [[Databases]]
1. **Conceptual data models and entity relationship modelling**
2. **Relational databases**
3. **Database design and normalisation techniques**
4. **Structured Query Language (SQL)**
5. **Client server databases**


Databases never store more than 1 piece of data in a item. Items must be ordered in terms of their data type.

**RELATIONAL DATABASE:** A database where the data is structured as a series of tables representing entities the database management software provides tools for joining the tables together, for example using primary and foreign keys**

- **Handling large sets of data much more efficient**
- **Reduces storage requirements**
- **Avoids redundancy**

**Field (attribute):** One piece of data about an object or person

**Primary Key:** field uniquely identifies each record and ensures all records are unique

**Table:** Data is stored within a table

**Record:** a row with all the data about an object or person

>In a relational database, data is separated into tables; each one stores data relating to a single type of entity. An entity is something in the real world that is represented in a database, for example a product in a shop.

To go from a flat file database to a relational database involves a process called NORMALISATION

A Foreign Key is a primary key from another table that is used to link the two tables together

| Name          | Description                                                                                                                                                                 | 
| ------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | 
| **Primary Key**   | used to ensure data in the specific column is unique                                                                                                                        |     
| **Entity**        | something in the real world represented in a database                                                                                                                       |     
| **Field**         | a property or characteristic of an entity                                                                                                                                   |     
| **Record**        | an instance of an entity                                                                                                                                                    |     
| **Foreign Key**   | column or group of columns in a relational database table that provides a link between data in two tables; it uniquely identifies a record in the relational database table |     
| **Table**         | Organised collection/storage of data                                                                                                                                        |
| **Normalisation** | process of converting data into a relational database following a series of rules                                                                                           |                                                                                                                                                                            |     |     |


### EXAM DEFINITIONS

| EXAM DEFINITIONS                                                                                                                       |
| -------------------------------------------------------------------------------------------------------------------------------------- |
| **RELATIONAL DATABASE:** An organised collection of related data, stored in tables linked by shared attributes (primary & foreign key) |
| **ENTITY:** an object about which data is stored                                                                                       |
| **FIELD:** A Category of information about an entity                                                                                   |
| **RECORD:** Instance of an entity                                                                                                      |
| **PRIMARY KEY:** Field / Attribute that unique identifies a record (1) FOREIGN KEY: Field / Attribute that refers to a primary key from another table (1)                                                                                                                                       |
`

*MULTI JOIN*:
```sql
SELECT Students.FirstName, Students.LastName, Classes.ClassCode, Staff.StaffInitials, Staff.FirstName, Staff.LastName
FROM Students
INNER JOIN ClassMembers ON Students.StudentNumber = ClassMembers.StudentNumber
INNER JOIN Classes ON ClassMembers.ClassCode = Classes.ClassCode
INNER JOIN Staff ON Staff.StaffInitials = Classes.StaffInitials
ORDER BY Students.LastName
```

![](https://uc23f274f2dfdc53c5c90e4b2b46.previews.dropboxusercontent.com/p/thumb/ACGdUH40y00JlVTuT9rzJX1huBYD4IWZabCgMiiImW1_3O52FfV6nWvJxu_337bs9mlXRTz_DUJZMvCcOUQ6EIj8ReJ_Nyw7eRoGGrzd2zqZXTG2tubZe7mPIqBRzdOyKvRxPNVdhrKxCjHuXDjJFDvXQm790QLWSGLkfTz3jfkgvXHXghDxT-yzDncLx2z99sKWA43d3yTbOxXnnoVNIEiMGCpRuoAYIP2bAiv8_9T1qX6MqjRew4rlLDvVFJAShcpGZoG_kPDWRjrpXwgt5GKVkTCglL--5hAs79176K4tkWUImbGw0C9WNTK4bAZC0gNPQshu51tH25Ls--4JoCpSyI9GKXozn4yIbqYcuLGL76J77w-Zs2nMVHvbtTn972E/p.png)

**Composite Primary Key:**
- `Sometimes two or even more attributes are needed to uniquely define a record`
- `For example, in a customer order consisting of many different order lines, each order line may be uniquely identified by the two attributes Primary and Foreign Key.`

Normalisation is a process used to come up with the best possible design for a database.
Tables should be organised so that data is not duplicated in the same table or in different tables.

There are three stages in normalisation:
- First Normal Form (1NF)
- Second Normal Form (2NF)
- Third Normal Form (3NF)

*First Normal Form (1NF):
- A table is in 1NF if it contains no repeating attributes or groups of attributes
- All attributes must be atomic - a single attribute cannot consist of two data items such as first name and surname

*Second Normal Form (2NF)
- A table is in 2NF if it is in the 1NF and contains no partial dependencies (we can only have dependencies if there is a composite primary key)

*Third Normal Form (3NF)
- A table is 3NF if it is in the 2NF and contains no non-key dependencies. this is defined by saying ”All attributes are dependent on the key, the whole key and nothing but the key”

>A partial dependency is when a non-prime attribute is functionally dependent on part of a primary key`
>A non-key dependency is when there are no fields that are dependent on other fields that are not part of the key.`
>A transitive dependency is when one non-prime attribute is dependent on another non-prime attribute.`

**C# - Double (float), String, Int, Bool, DATETIME 
SQL - Real / Float, Char(n) / Varchar(n), Int, Boolean / BIT, DATETIME

*UNIQUE(1,1) counter increment starts at 1 and increments by 1 
```sql
CREATE TABLE Students
(
StudentID int, IDENTITY(1,1) UNIQUE NOT NULL,
FirstName VARCHAR(100) NOT NULL,
LastName VARCHAR(100) NOT NULL,
PRIMARY KEY (StudentID)
)

CREATE TABLE ClassMembers
(
StudentID int NOT NULL,
ClassCode CHAR(6) NOT NULL,
CONSTRAINT FK_StudentsClassMembers
FOREIGN KEY (StudentID)
REFERENCES Students(StudentID),
CONSTRAINT FK_ClassesClassMembers
FOREIGN KEY (ClassCode)
REFERENCES Classes(ClassCode)
PRIMARY KEY (StudentID, ClassCode)
)

CREATE TABLE Staff
(
StaffID int, IDENTITY(1,1) UNIQUE NOT NULL,
FirstName VARCHAR(100) NOT NULL,
LastName VARCHAR(100) NOT NULL,
StaffInitials CHAR(3) NOT NULL,
PRIMARY KEY (StaffID)
) 
```

Fields are between brackets Identifier is first, then the data type

Constraints are: NOT NULL, UNIQUE There is no string or double data type in SQL The foreign key is the most difficult bit to remember.
- SQL is used to create and manage relational databases.
- Normalization is the process of optimizing the design of a database to minimize redundancy and improve efficiency.
- DDL (Data Definition Language) is a subset of SQL used to create and modify the structure of a database.
