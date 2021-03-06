## Conditional expressions
`IF... THEN...ELSE...ENDIF` is the most common conditional statement. SQL has a `CASE` statement and a `CASE` expression. The latter can be use in the following ways:
* Use the expression with search condition.
* Use the expression to compare a table field to a specified value.

### CASE with search conditions
This has the following syntax,
```
CASE
  WHEN condition_1 THEN result_1
  WHEN condition_2 THEN result_2
  ...
  WHEN condition_n THEN result_n
  ELSE result_m
END
```
Example updating values using CASE expression
```
UPDATE GRADES
SET MIDTERMS = CASE
    WHEN SCORE >= 90
      THEN 'A'
    WHEN SCORE >= 80 AND < 90
      THEN 'B'
    WHEN SCORE >= 70 AND < 80
      THEN 'C'
    ELSE 'D'
END;
```

### CASE with values
CASE with values has similar syntax with search conditions except condition is replaced with values
```
CASE test_value
  WHEN value_1 THEN result_1
  WHEN value_2 THEN result_2
  ...
  WHEN value_n THEN result_n
  ELSE result_m
```

### CASE NULLIF
```
UPDATE FLIGHT                                         # This is in a shorthand form
SET Connection = NULLIF(Connection, 'Chicago');
```

### CASE - COALESCE
This has the following form
```
CASE
  WHEN value_1 IS NOT NULL
    THEN value_1
  WHEN value_2 IS NOT NULL
    THEN value_2
  ...
  WHEN value_n IS NOT NULL
    THEN value_n
  ELSE NULL
END
```

## Data-type conversions

### CAST
```
SELECT *
FROM CUSTOMERS
WHERE CUSTOMERS.ID = CAST (PROSPECT.ID AS INTEGER)
```

## Modifying clauses
Modifying cluases available in SQL are FROM, WHERE, HAVING, GROUP BY, and ORDER BY. They must appear in the following order:
```
SELECT column_list
FROM table                      # Specifies the table
WHERE search_condition          # Filters out rows
GROUP BY grouping_column        # Separates rows into groups
HAVING search_condition         # Filters out groups
ORDER BY ordering_condition;    # Sorths the results of prior clauses
```

### WHERE
```
SELECT column_list
FROM table_name
WHERE condition;
```

### BETWEEN
```
SELECT FirstName, LastName
FROM GRADES
WHERE GRADES.Score BETWEEN 80 AND 100
```

### IN and NOT IN
```
SELECT FirstName, LastName
FROM CUSTOMERS
WHERE State IN ('CA', 'NY', 'NJ')

SELECT FirstName, LastName
FROM CUSTOMERS
WHERE State NOT IN ('CA', 'NY', 'NJ')
```

### LIKE and NOT LIKE
* % is a wildcard that can stand for any string of characters that have zero or more characters.
* _ is a wildcard for any single character.
* '#' is an escape character.
```
SELECT FirstName
FROM CUSTOMERS
WHERE LastName LIKE 'Br%';
```

### NULL and NOT NULL
```
SELECT FirstName, LastName
FROM CUSTOMERS
WHERE Phone IS NOT NULL;
```

### UNIQUE
Unique predicate is use with a subquery.
```
SELECT FirstName, LastName
FROM CUSTOMER
WHERE UNIQUE
  (SELECT OrdersID FROM ORDERS
   WHERE ... )
```

### DISTINCT
Distinct is similar to unique except it is use for nulls.

## Logical connectives

### AND
Multiple conditions must be true to get results when using `AND`.
```
SELECT FirstName, LastName
FROM CUSTOMERS
WHERE State = 'CA' AND State = 'NY';
```

### OR
One of two or more conditions must be true to get results when using `OR`.
```
SELECT FirstName, LastName
FROM CUSTOMERS
WHERE State = 'CA'OR State = 'NY';
```

### NOT
Negates the condition.
```
SELECT FirstName, LastName
FROM CUSTOMERS
WHERE NOT (State = 'CA');
```

### GROUP BY
```
SELECT *
FROM CUSTOMERS
GROUP BY State;
```

### HAVING
Acts as a filter on groups rather than on individual rows.
```
SELECT FirstName, LastName
FROM CUSTOMERS
GROUP BY State
HAVING State <> 'CA';
```

### ORDER BY & FETCH
Display the query in ascending or descending order.
```
SELECT *
FROM ORDERS
ORDER BY OrderDate ASC, Quantity DESC
OFFSET 5 ROWS                           # Tells how many rows to skip
FETCH NEXT 10 ROWS ONLY;                # Gets the next 10 rows
```
