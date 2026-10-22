# Database
#### An organized collection of related data stored electronically and managed by a Database Management System (DBMS).

## Database Management System (DBMS)
System that handles:
- Storage
- Access control
- Security
- Integrity
- Transactions


### File System vs Database System
| Feature | File System | Database |
|----------|----------|----------|
| Structure   | Separate files   | Centralized   |
| Redundancy   | High   | Reduced   |
| Security   | Weak   | Strong   |
| Integrity   | Not enforced   | Enforced   |

### Advantages
- Reduced redundancy --> Minimizing duplication of data within a database by storing each piece of information only once and linking related data using keys.
- Improved consistency --> Ensuring data remains accurate and uniform throughout the database. Changes made in one place are correctly reflected everywhere it is used.
- Better security --> Protecting data from unauthorized access, modification, or deletion by using authentication, authorization, and access control mechanisms.
- Faster querying --> Retrieve specific data efficiently from large datasets using structured queries, indexing, and optimized search mechanisms.
- Data sharing --> Allow multiple authorized users or systems to access and use the same centralized database simultaneously.
- Concurrency control --> Ensures multiple users can access or modify data at the same time without causing conflict or inconsistencies.
- Backup and Recovery --> Process of creating copies of data and restoring  the database to a consistent state after system failure or data loss.

---
## Relational Database
System that organizes data into structured table

### Table
Consists of:
- Rows (records/tuples)
- Columns (fields/attributes)

Example: STUDENT TABLE
| StudentID (PK) | Name | Age |
|----------|----------|----------|
| 0   | Guy   | 17   |
| 1   | Reed   | 19   |

#### The first row holds the labels (start at row index 1)
#### The first column holds the index (start from 0)

### Keys
- Primary Key (PK) --> Uniquely identifies a record
- Foreign Key (FK) --> Links tables

### Benefits:
- Data integrity enforces rules to ensure data is accurate and valid
- Data consistency ensures that all users see the same correct data, with no conflicting updates occur
- Concurrency control allows multiple users to access the database simultaneously wihtout conflict
- Reliable transaction processing (ACID)
  - Atomicity --> All or nothing
  - Consistency --> Valid state maintained
  - Isolation --> Transactions do not interfere
  - Durability --> Changes are permanent
- Data retrieval (SQL)
- Secure, providing authentication and authorization
- Can handle growing data and users
- Widely used, has strong documentation

### Limitations:
- Rigid schema
  - Requires a predefined structure
  - Hard to modify later
- Requires careful planning, normalization, relationship mapping
- Strugles with large data
- Unstructured daa handling
- Hierarchical data handling
- Object-relational impedance mismatch

---

## Relationships
### One-to-One (1:1)
- One record <--> one record
- Oftern share PK or use FK

### One-to-Many (1:M)
- One record --> many records
- FK is on the many side

### Many-to-Many (M:M)
- Cannot be implemented directly
- Must usa a junction table (table containing PK of table A and table B)

#### Example: Composite PK = (tableAID, tableBID)

This is to:
- avoid redundancy
- resolve many-to-many relationship

---

## Database Schema
Blueprint or structure of a database.

#### Defines:
- What data is stored
- How it is organized
- How different parts relate

#### Levels of abstraction:
1. Conceptual schema
2. Logical schema
3. Physical schema

### Conceptual Schema
Describes the database at the highest level of abstraction.

#### Focus:
- What data is needed
- What are the main entities
- What is the relationship between the entities

#### No technical details yet.

### Logical Schema
Translates the conceptual schema into a structured format that a database system can understand.

#### Contains:
- Tables
- Columns (attributes)
- Data types
- Primary keys
- Foreign keys
- Constraints

### Physical Schema
Describes how the database is actually stored and implemented on hardware.

#### Includes:
- File structures
- Indexes
- Storage allocation
- Access methods

---

## Database Normalization
The process of organizing data in a database to reduce redundancy and improve data integrity and consistency.

In short: Dividing large tables into smaller, related tables.

#### Unnormalized table:
- Duplicate data
- Unorganized

#### Normalized table:
- Reduced duplicates
- Organized
- Consistent

## Problems without normalization
### Update Anomaly
When a value must be updated in many places.

### Insertion Anomaly
When new data cannot be added without other unrelated data.

### Deletion Anomaly
When deleting a record unintentionally removes important data.

## Forms of Normalization
### First Normal Form (1NF)
- Each field contains atomic (indivisible) values
- No repeating groups
- Each record can be easily identified by a primary key

### Second Normal Form (2NF)
- Must be in 1NF
- All non-key attributes depend on the entire primary key (No partial dependecies)

### Third Normal Form (3NF)
- Must be in 2NF
- No transitive dependencies

## Types of Dependencies
### Partial dependency
A non-key attribute is dependent on only a part of a primary key.

### Transitive dependency
A non-key attribute depends on another non-key attribute.

---
