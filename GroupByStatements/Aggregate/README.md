#### GROUP BY Definition
- GROUP BY will allow us to aggregate data and apply functions to better understand how data is distributed per category.

#### Aggregate Functions
- SQL provides variety of aggregate functions.
- The main idea behind an aggregate function is to take multiple inputs and return a single output.

https://www.postgresql.org/docs/9.5/functions-aggregate.html

#### Most Common Aggregate Functions
Note: Aggregate functions calls happen only in the SELECT clause or the HAVING clause.

#### Special Notes to learn about aggeragate function AVG() and COUNT()
- AVG() returns a floating point value many decimal places (eg: 2.345353).
- We can use ROUND() aggregate function to specify precision after the decimal from AVG() function.

Example: 
```sql
SELECT MAX(repleacement_cost) from film;
```

```sql
SELECT ROUND(AVG(repleacement_cost),2) from film;
```



