#### SELECT ...... FROM ...... WHERE conditions
- The WHERE statement allows us to specify conditions on columns for the rows to be returned.
- The Where clause appears immediately after the from clause of the statement.

Basic Sytax:
```sql
SELECT column1, column2
FROM table
WHERE conditions;
```

Conditions or Operators provided by PostgreSQL for the WHERE Clause? 
- Comparision Operators that compares column value to something. Is the price greater than 3. pet's name = "Sam".
- Logical Operators allows us to combine multiple comparision operators. AND,OR,NOT.

Example:
```sql
SELECT name,choice FROM table WHERE name = 'David' AND choice = 'Red';
``` 