# 4.10 Fundamentals of Databases

Databases never store more than 1 piece of data in a item. Items must be ordered in terms of their data type.

**RELATIONAL DATABASE:** A database where the data is structured as a series of tables representing entities the database management software provides tools for joining the tables together, for example using primary and foreign keys**

- **Handling large sets of data much more efficient**
- **Reduces storage requirements**
- **Avoids redundancy**

**Field (attribute):** One piece of data about an object or person

**Primary Key:** field uniquely identifies each record and ensures all records are unique

**Table:** Data is stored within a table

**Record:** a row with all the data about an object or person

![](https://uc4066043e2212b2bda7d923b0a7.previews.dropboxusercontent.com/p/thumb/ACFx7vmie17oH4i3qBMl-1Nv5kCWFDwlbo3iCH-kEDa9DhKlLDb9ZId0TJtAfwEzgRx3PaajWlKp0dOUiO2lLSYEsic-PvZz_g34bMClunCUhFTgDJYhq6lKb27CRh6yFZCLOU_6DciswFcos_9NYPrFbk1WGbTR0-xCg8-fpCXZE-L96EdeC4kEVinxL_PsMgV3kVhIkz-_DLq9TERdHyHylDCT4phOAXDzfpfBZhalMl027yJjpCRxWEngYcdWdMBg7h3KSljHNHKmdxWJcFc-_duNEt9kHT2OQynEehQmrAniVRo2RSG6kjTTTqf7XjYcSU46AEInq3Kva5c8DLBytCJCVFGC5BEAP9KBE_ynB8NhIrg_HRRAhOIpkdxdZfM/p.png)

>In a relational database, data is separated into tables; each one stores data relating to a single type of entity. An entity is something in the real world that is represented in a database, for example a product in a shop.

To go from a flat file database to a relational database involves a process called NORMALISATION

A Foreign Key is a primary key from another table that is used to link the two tables together

![](https://uca812d4a97a57ec8ce39a804972.previews.dropboxusercontent.com/p/thumb/ACF_FnST_J90iSxJ8rHNTEyVPMCEHQG3S0e7u0wley-8b_f9_wPNdIBuV_LYoikLQEMR5JfIAPJH7yHoa2l4lv9CnQo0UPQzjC30gWLUZVsWd-XBGltbd1pLJnxQg_FJCWf0TQLmUJ807QtNcgmd23pl_jfxX7Qh1Krz3Rvkx8fRKHpw6PUH28l-TpAyHcL2RXQJxxvGO_mFzTUX30hl_sUN7ZYfngVXc-XctKmkUkK7PoUmBLqGJlCUrL4in3xOspzxh9xaTR0b7_dWdeZX5Xxmw5BX34W8XHOKFao3UoGtQ9Y73YR64JJqoEyAUEmTsgPnP-ycSu2xk3KxKeYJAM2rw0QbFUIlCB9R2cYb05Hv7vbQYZTMa0itXevLGdwj8mg/p.png)

A local free recycling group has been set up in a small community. If Member A no longer needs an item, he can advertise it on the group’s website. If Member B needs an item, she can search for it on the site. The two members then get in contact and Member A gives the item to Member B.

Items are removed from the site when exchanged or after six weeks. The scheme is based on a relational database, which includes the two tables, Member and Item.

(a) Complete the definition below.

A relational database is a collection of **TABLES REPRESENTING ENTITIES** in which relationships are created through database management software

EXAM DEFINITIONS

**RELATIONAL DATABASE:** An organised collection of related data, stored in tables linked by shared attributes (primary & foreign key) 
**ENTITY:** an object about which data is stored
**FIELD:** A Category of information about an entity 
**RECORD:** Instance of an entity 
**PRIMARY KEY:** Field / Attribute that unique identifies a record (1) FOREIGN KEY: Field / Attribute that refers to a primary key from another table (1)`

MULTI JOIN:
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

![](https://ucf34864eab6d2dcaddbd9c8c301.previews.dropboxusercontent.com/p/thumb/ACFszgqSH99mCExK3rJjfRbkKmJv2LN-bZ37Xa7R25vkxbcHkJiK88oUWTVppT9tWSrKrYgtN96q0tRxtenuFaQDEsllFb9nzn-BK4ONIFRc9-iKkXRijPN7iYHJR8DKRSfKHuUXGIoift24hmah_tyNXOzwsGMwsb2wV2wob4E8jgIe9uTWiAklyor1Q6UACRSxdx-jiaWW1C1o-AjELu6C1P2cc0GWretCl8q1f2F6AWMjCCACMMh2KVWI24SAn6Q6MhF1zwVoUqz0yKcdHLrMALWHTqD8AZ-Njy7Cf72LcEtYT79R-EvuJuP0KQiykgOafC_MD-XB-6oeE7rTImQakB0PKK832VwUbhnZoED-hZT7O-vRQYyCQI6m7vFSDWM/p.png)
![](https://uc60e00a876344f3646cba9dc840.previews.dropboxusercontent.com/p/thumb/ACGGWI4nrdcnHM1oL1KeJ0npIGKrTM0HNNR2793NyxfCIsSo232g5FEjHlXAM4NR2fkFfKJ59IFcVb4Cb0r7w4O-OxifbRKRTk_B_h0YdwVdm5Dt3JW5-YCIRFpJWmhMfRkiJFeKHjMQQtnw3ins-RkdGiOgQw0isb8RTfwMg61IVsS2GdTBNmrtEJ6mETognTKoki6NFTX5aePXVgnxcttJEnrpPBs41e3-DDp_B4h1Vdr-0rQpe_uDudmf-rymssK_PTA5m_F9D4BdfyZBKvJW4wgo2aPZs3U3fOf8xwcZ80Yrc8rMHy5Aelw2eSbC279pQCTfhp8SLbZWtbJf4nkF-h89p75Ptcw2xCODXiBQW42F1tjY7WDowcVNMXH9utY/p.png)
![](https://uca9e362d97b3d71ee677179e008.previews.dropboxusercontent.com/p/thumb/ACF3m1jEWtvaY9qOX7ZFrfelW4MktuU31P3hbpwo-hjbVl4Oj6NcBrW1lGBVU8oFA_gnzJQNFshjnVF9qe19w_p1Ds4KrJvcMTRafEGY1PzgSAR59D_L4839qOGhgxQyUiYgtZ4lJFK1r2jCUpIGYVnD5L8t-8B6hjcPghrHtRWWiyvH51oZU0kCxhCagOgLm6ds-tviyUqLvS6dw31jEYSl-1oGQmvYClmajyD28KrIaKpQMlSrZaeaSdx9jeqAI3y3bHZiNV-Ta5G4p80rqTNi_HNDVlzx-J588sIXktRLU4YSbCUJXj-Q_lb1ES0OHrWLSXfRke4elzIZgkBpZ54Ct17WjG--g7-u2oiqv-DmZsQSm9c0apEuPzV0Q1_rbSg/p.png)

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
