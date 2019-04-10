* [FMDB](https://github.com/ccgus/fmdb)
  * SQLite
  * executeUpdate
  * executeQuery
  * executeStatements
  * changes
  * [user_version](https://github.com/ccgus/fmdb/issues/210)

* [SQLite Tutorial](https://www.tutorialspoint.com/sqlite/index.htm)
  * [Datatypes in SQLite](https://www.sqlite.org/datatype3.html)
    * INTEGER
    * REAL
    * TEXT
    * BLOB
  * [GROUP BY](https://www.tutorialspoint.com/sqlite/sqlite_group_by.htm)
  * [JOINS](https://www.tutorialspoint.com/sqlite/sqlite_using_joins.htm)
    * Cross Join
    * Inner Join
    * Outer Join - Only left outer join
  * Index
    * [Index](https://www.tutorialspoint.com/sqlite/sqlite_indexes.htm)
    * [Indexed By Clause](https://www.tutorialspoint.com/sqlite/sqlite_indexed_by.htm)

* [DB Browser for SQLite](https://sqlitebrowser.org)

* Create Table
``` SQL
CREATE TABLE IF NOT EXISTS device (
    uuid TEXT NOT NULL,
    name TEXT,
    info TEXT,
    created REAL NOT NULL,
    updated REAL NOT NULL
);

PRIMARY KEY

AUTOINCREMENT

DEFAULT
```

* Alter Table
```SQL
ALTER TABLE device ADD COLUMN manufacturer TEXT;
```

* INSERT INTO
```SQL
INSERT INTO device (uuid, name, info, created, updated)
VALUES ('5cb2d6f7-8e99-474f-8998-6a8135f33456', 'the red device', '', 1554790063.342, 1554790063.342);
```

* SELECT
```SQL
SELECT * FROM device;

SELECT uuid, name FROM device;
```

* UPDATE
``` SQL
# update all
UPDATE device
SET name = 'the green device', info = 'some information', updated = 1554791346.762;

# update, with WHERE clause
UPDATE device
SET name = 'the green device', info = 'some information', updated = 1554791346.762
WHERE uuid = '5cb2d6f7-8e99-474f-8998-6a8135f33456'
```

* DELETE
```SQL
# delete all
DELETE FROM device;

# delete, with WHERE clause
DELETE FROM device WHERE uuid = '5cb2d6f7-8e99-474f-8998-6a8135f33456';
```

* Operator
  * [LIKE](https://www.tutorialspoint.com/sqlite/sqlite_like_clause.htm)
```SQL
Arithmetic: +    -    *    /    %
Comparison: =    !=    >    <    >=    <=
Logical: AND    OR    EXISTS    IN    NOT IN    LIKE    IS NULL    IS NOT NULL
Bitwise: &    |    <<    >>
```

* WHERE
  * Specify a condition
  * AND
  * OR

* ORDER
```SQL
SELECT *
FROM ...
WHERE ...
ORDER BY created ASC;

SELECT *
FROM ...
WHERE ...
ORDER BY updated DESC;

SELECT *
FROM ...
WHERE ...
ORDER BY created ASC, updated DESC;
```

* LIMIT
```SQL
SELECT * FROM device ORDER BY updated DESC LIMIT 1
```

* ALIAS
```SQL
SELECT uuid, (updated - created) as diff FROM device;
```

* DISTINCT
```SQL
SELECT DISTINCT name FROM device;
```

* COUNT

* MIN

* MAX

* AVG

* SUM
