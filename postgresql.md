1) Question: 
What will happen (assuming permissions are fine and storage is in place)?
```sql
BEGIN;
CREATE TABLESPACE myspace LOCATION 'data';
```

Possible answers:
 - It works
 - It will error out
 - It will issue a warning
 
 Source: http://www.cybertec.at/en/quiz/
 
2) Question:
What is the correct result?
```sql
SELECT 3 = ALL ('{}'::int[]);
```
 
Possible answers:
 - NULL
 - False
 - True
  
Source: http://www.cybertec.at/en/quiz/

3) Question:
What is the correct result?
```sql
SELECT 3 = ANY ('{}'::int[]);
```

Possible answers:
 - False
 - True
 - NULL
  
Source: http://www.cybertec.at/en/quiz/

4) Question:
What is the correct result?
```sql
SELECT NULL IS NULL IS NULL;
```

Possible answers:
 - True
 - False
 - NULL
  
Source: http://www.cybertec.at/en/quiz/
  
5) Question:
now() can be used to determine transaction time. But what happens in a subtransaction?
```sql
BEGIN;
SELECT now();
SAVEPOINT a;
SELECT now();
```

Possible answers:
 - different results
 - an error will happen
 - same result
 
Source: http://www.cybertec.at/en/quiz/

6) Question:
What will happen?
```sql
BEGIN;
SAVEPOINT a;
CREATE TABLE x (x int);
SAVEPOINT a;
ROLLBACK TO SAVEPOINT a;
```
Is there a table there or not?

Possible answers:
 - yes, it is there
 - no, it is not there
 - this one will error out
  
Source: http://www.cybertec.at/en/quiz/

7) Question:
Which column are you going to get?
```sql
BEGIN;
CREATE TABLE x (x int);
CREATE TEMP TABLE x (y int);

SELECT * FROM x;
```

Possible answers:
 - This will error out all
 - The "temporary table" will be shown
 - The "real table" will be shown
  
Source: http://www.cybertec.at/en/quiz/

8) Question:
What will be the answer?
```sql
SELECT COUNT(*)
FROM (VALUES (1), (2)) t ( v )
WHERE v NOT IN (3, 4, NULL);
```

Possible answers:
 - 0
 - NULL
 - 2
  
Source: http://www.cybertec.at/en/quiz/

9) Question:
How many rows will the SELECT return?
```sql
CREATE TABLE x (id int);
INSERT INTO x VALUES (0), (NULL);
SELECT * FROM x WHERE id <> 0;
```

Possible answers:
 - 1
 - 2
 - 0
  
Source: http://www.cybertec.at/en/quiz/

10) Question:
What is the correct answer?
```sql
SELECT COUNT(DISTINCT t) 
FROM (VALUES (1), (2), (NULL), (NULL)) t ( v );
```

Possible answers:
 - 3
 - 4
 - 2
  
Source: http://www.cybertec.at/en/quiz/

11) Question:
What is the correct answer?
```sql
SELECT COUNT(v) 
FROM (VALUES (1), (2), (NULL), (NULL)) t ( v );
```

Possible answers:
 - 2
 - 3
 - 4
  
Source: @NikolayS

11) Question:
What is the correct answer?
```sql
SELECT COUNT(t) 
FROM (VALUES (1), (2), (NULL), (NULL)) t ( v );
```

Possible answers:
 - This will error out
 - 4
 - 2
  
Source: @NikolayS
