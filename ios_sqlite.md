* [FMDB](https://github.com/ccgus/fmdb)
  * SQLite
  * executeUpdate
  * executeQuery
  * executeStatements
  * changes
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
    created REAL,
    updated REAL
);
```

* NULL
``` SQL

```

* INSERT INTO
```SQL
INSERT INTO device (uuid, name, info, created, updated)
VALUES ('5cb2d6f7-8e99-474f-8998-6a8135f33456', 'the red device', '', 1554790063.342, 1554790063.342);
```

```SQL
INSERT INTO
Insert data in specific columns
```

* UPDATE
``` SQL
UPDATE device
SET name = 'the green device', info = 'some information', updated = 1554791346.762;

UPDATE device
SET name = 'the green device', info = 'some information', updated = 1554791346.762
WHERE uuid = '5cb2d6f7-8e99-474f-8998-6a8135f33456'
```

``` SQL
Update Table
UPDATE Multiple records

```

* DELETE
```SQL
DELETE FROM device WHERE uuid = '5cb2d6f7-8e99-474f-8998-6a8135f33456';
DELETE FROM device;
```

* SELECT
```SQL
SELECT *
FROM device
WHERE uuid = 5cb2d6f7-8e99-474f-8998-6a8135f33456
ORDER BY created ASC;

SELECT *
FROM device
ORDER BY updated DESC;

SELECT *
FROM device
ORDER BY created ASC, updated DESC;

SELECT uuid, name
FROM device;
```

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
