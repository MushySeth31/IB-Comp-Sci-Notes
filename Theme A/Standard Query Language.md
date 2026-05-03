# Standard Query Language
#### A programming language used to communicate with relational databases (retrieve, insert, update, delete data)

---

## Core SQL Categories
### Data Query Language (DQL)
Retrieve data from a database.

#### Commands: `SELECT`

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

inline:
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
