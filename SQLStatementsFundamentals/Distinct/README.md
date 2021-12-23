#### SELECT DISTINCT ..... FROM .....
- Table contains a column that has duplicate values, we may end up in a situation where we just want to list distinct or unique values in that column.
DISTINCT Keyword can be used to return only the distinct values in a column.

Basic Sytax:
```sql
SELECT DISTINCT column FROM table
```

Example:
```sql
SELECT DISTINCT name FROM color_table;
SELECT DISTINCT(release_year) FROM film;
``` 