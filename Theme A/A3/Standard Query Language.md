# Standard Query Language
#### A programming language used to communicate with relational databases (retrieve, insert, update, delete data)

---

## Core SQL Categories
### Data Query Language (DQL)
Retrieve data from a database.

#### Commands: 
`SELECT`

### Data Manipulation Language (DML)
Modify data stored in tables.

#### Commands:
- `INSERT`
- `DELETE`
- `UPDATE`

### Data Definition Language (DDL)
Define or modify the structure of database objects.

#### Commands:
- `CREATE`
- `ALTER`
- `DROP`

### Data Control Language (DCL)
Control access to the database.

#### Commands:
- `GRANT`
- `REVOKE`

---

## Syntax list
### SELECT
Retrieve data from one or more tables.

#### Example:
```sql
SELECT column_name
FROM table_name;
```

Inline:
```sql
SELECT column_name FROM table_name;
```

To retrieve multiple fields:
```sql
SELECT column1, column2
FROM table_name;
```

To retrieve all fields:
```sql
SELECT *
FROM table_name;
```

### WHERE
Filter records based on specific conditions.

#### Example:
```sql
SELECT column_name
FROM table_name
WHERE conditions;
```

#### Comparison Operators
| Operator | Meaning |
| --- | :--- |
| = | equal |
| != / <> | not equal |
| >, < | greater/less |
| >=, <= | greater/less or equal to |

#### Logical Operators
```sql
SELECT * FROM STUDENT
WHERE Age = 18 AND Name = 'John';
```
- `AND` --> both true
- `OR` --> at least one true

### ORDER BY
Sort the result by query.

#### Example:
```sql
SELECT Name FROM Student
ORDER BY Name ASC;
```
- `ASC` --> ascending (default arrangement)
- `DESC` --> descending

### INSERT
Add new records to a table.

#### Example:
```sql
INSERT INTO STUDENT (StudentID, Name, Age)
VALUES ('ID3', 'Alex', 17);
```

### UPDATE
Modify existing table.

#### Example:
```sql
UPDATE STUDENT
SET Age = 18
WHERE StudentID = 'ID3'
```

#### If no `WHERE` --> updates ALL records

### DELETE
Remove a record from table.

#### Example:
```sql
DELETE FROM STUDENT
WHERE StudentID = 'ID3';
```

#### If no `WHERE` --> deletes entire table data
