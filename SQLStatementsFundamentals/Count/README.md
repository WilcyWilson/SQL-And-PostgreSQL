#### SELECT COUNT(column) FROM ......
- COUNT query returns the number of columns of a table which is same for all the columns as we know.
- We can apply count on a specific column or use * that define all column.

Basic Sytax:
```sql
SELECT COUNT(name) FROM table
```

Example:
```sql
SELECT COUNT(name) FROM table;
SELECT COUNT(*) FROM film;
``` 

Using COUNT and DISTINCT as together
```sql
SELECT COUNT(DISTINCT name) FROM table;
``` 