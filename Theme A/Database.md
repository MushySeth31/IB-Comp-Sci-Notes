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

#### Example: STUDENT(StudentID, Name, Age)

### Keys
- Primary Key (PK) --> Uniquely identifies a record
- Foreign Key (FK) --> Links tables

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


