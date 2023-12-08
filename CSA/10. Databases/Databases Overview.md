# 4.10 Fundamentals of Databases

Databases never store more than 1 piece of data in a item. Items must be ordered in terms of their data type.

**RELATIONAL DATABASE: A database where the data is structured as a series of tables representing entities the database management software provides tools for joining the tables together, for example using primary and foreign keys**

- **Handling large sets of data much more efficient**
- **Reduces storage requirements**
- **Avoids redundancy**

Field (attribute): One piece of data about an object or person

Primary Key: field uniquely identifies each record and ensures all records are unique

Table: Data is stored within a table

Record: a row with all the data about an object or person

![https://www.dropbox.com/scl/fi/a5h9u48gjs9qmhodqyfyx/SQL1.png?rlkey=s0b2d9h41qjq693bd1u4klbxf&dl=0]
In a relational database, data is separated into tables; each one stores data relating to a single type of entity. An entity is something in the real world that is represented in a database, for example a product in a shop.

1. What entities do we need for our database? I’ll start you off. We need:

- a student entity/table.
- a staff entity/table.

1. What fields/attributes will be stored about each one?

- The student table will store their first name and surname, address, student address, secondary school, gcse avg, contact number, classes`
- The staff table will store their first name and surname, address, contact information

1. Can you identify which of the attributes will form the primary key for each table?

- Student ID
- Staff ID

To go from a flat file database to a relational database involves a process called NORMALISATION

A Foreign Key is a primary key from another table that is used to link the two tables together

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b6ab040a-a6ce-4f2d-b198-32467a3e6dac/Untitled.png)

A local free recycling group has been set up in a small community. If Member A no longer needs an item, he can advertise it on the group’s website. If Member B needs an item, she can search for it on the site. The two members then get in contact and Member A gives the item to Member B.

Items are removed from the site when exchanged or after six weeks. The scheme is based on a relational database, which includes the two tables, Member and Item.

(a) Complete the definition below.

A relational database is a collection of **TABLES REPRESENTING ENTITIES** in which relationships are created through database management software

EXAM DEFINITIONS

- `RELATIONAL DATABASE: An organised collection of related data (1), stored in tables linked by shared attributes (primary & foreign key) (1)`
- `ENTITY: an object about which data is stored (1)`
- `FIELD: A Category of information about an entity (1)`
- `RECORD: Instance of an entity (1)`
- `PRIMARY KEY: Field / Attribute that unique identifies a record (1) FOREIGN KEY: Field / Attribute that refers to a primary key from another table (1)`

MULTI JOIN:

```sql
SELECT Students.FirstName, Students.LastName, Classes.ClassCode, Staff.StaffInitials, Staff.FirstName, Staff.LastName
FROM Students
INNER JOIN ClassMembers ON Students.StudentNumber = ClassMembers.StudentNumber
INNER JOIN Classes ON ClassMembers.ClassCode = Classes.ClassCode
INNER JOIN Staff ON Staff.StaffInitials = Classes.StaffInitials
ORDER BY Students.LastName

```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/582d5b5f-3d76-4ad6-ac57-251b48980027/Untitled.png)

`Composite Primary Key:`

- `Sometimes two or even more attributes are needed to uniquely define a record`
- `For example, in a customer order consisting of many different order lines, each order line may be uniquely identified by the two attributes Primary and Foreign Key.`

Normalisation is a process used to come up with the best possible design for a database.

Tables should be organised so that data is not duplicated in the same table or in different tables.

There are three stages in normalisation:

- First Normal Form (1NF)
- Second Normal Form (2NF)
- Third Normal Form (3NF)

First Normal Form (1NF):

- A table is in 1NF if it contains no repeating attributes or groups of attributes
- All attributes must be atomic - a single attribute cannot consist of two data items such as first name and surname

Second Normal Form (2NF)

- A table is in 2NF if it is in the 1NF and contains no partial dependencies (we can only have dependencies if there is a composite primary key)

Third Normal Form (3NF)

- A table is 3NF if it is in the 2NF and contains no non-key dependencies. this is defined by saying ”All attributes are dependent on the key, the whole key and nothing but the key”

`A partial dependency is when a non-prime attribute is functionally dependent on part of a primary key`

`A non-key dependency is when there are no fields that are dependent on other fields that are not part of the key.`

`A transitive dependency is when one non-prime attribute is dependent on another non-prime attribute.`

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/565fe01e-ceb0-49bf-9ac2-0bc06eb87b62/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/152e9af7-c8bf-441e-bbb8-5331b597b7eb/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4db7d798-52ef-4b68-b037-713dfbad8c32/Untitled.png)

C# - Double (float), String, Int, Bool, DATETIME SQL - Real / Float, Char(n) / Varchar(n), Int, Boolean / BIT, DateTime

Data Definition Language (DDL) is a subset of SQL. It is the SQL used to create all the tables and relations in a database. You need to be able to write this in the exam.

What things do you think we need to put in the space and brackets below to create a table of students for a college database?

UNIQUE(1,1) counter increment starts at 1 and increments by 1

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
