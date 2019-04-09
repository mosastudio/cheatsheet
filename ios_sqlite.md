* [FMDB](https://github.com/ccgus/fmdb)
  * SQLite
  * executeUpdate
  * executeQuery
  * executeStatements
  * [user_version](https://github.com/ccgus/fmdb/issues/210)

* [SQL Examples, w3schools](https://www.w3schools.com/sql/sql_examples.asp)

* [Datatypes in SQLite](https://www.sqlite.org/datatype3.html)
  * INTEGER
  * REAL
  * TEXT
  * BLOB

* Create Table
``` SQL
CREATE TABLE IF NOT EXISTS device (
    uuid TEXT,
    name TEXT,
    info TEXT,
    deleted INTEGER,
    created REAL,
    updated REAL
);

CREATE TABLE IF NOT EXISTS bpms (
    version INTEGER,
    origin INTEGER,
    begin REAL,
    end REAL,
    min INTEGER,
    max INTEGER,
    details BLOB
);
```

* NULL
``` SQL

```

* INSERT INTO
```SQL
INSERT INTO
Insert data in specific columns
```

* UPDATE
``` SQL
Update Table
UPDATE Multiple records

```

* DELETE
```SQL
DELETE FROM customers WHERE %@ < %f
DELETE FROM %@
```

* SELECT
```SQL
SELECT Column
SELECT *
SELECT DISTINCT
SELECT COUNT(DISTINCT column)

SELECT TOP
LIMIT
SELECT TOP PERCENT
SELECT TOP and add a WHERE Clause

Alias for columns
```

* 
```SQL
MIN
MAX
COUNT
AVG
SUM
```

* WHERE
```SQL
AND
OR
NOT

IS NULL
IS NOT NULL

IN
NOT IN

BETWEEN?
```

* ORDER BY
```SQL
ORDER BY
ORDER BY DESC
ORDER BY Several Columns
```

* JOINS
```SQL
INNER JOIN
LEFT JOIN
RIGHT JOIN
Self JOIN
```