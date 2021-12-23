
#### SELECT ...... FROM ...... ORDER BY .....
- We have noticed PostgreSQL sometimes returns same request query results in a different order each time. In order to remove this we can sort rows based on a column value in either ascending or descending order.
- Alphabetical for string based columns and numeric order for numerical columns.

Basic Sytax:
```sql
SELECT column1, column2
FROM table
ORDER BY column_1 ASC/DESC;
```

Using ORDER BY in multiple column? What does this mean?
- This makes sense when one column has duplicate entires. Notice we have duplicate entries in company column. If we were to actually order by two columns here.
- Here ordering by first company then by sales. This means we sort everything based off the company column first. After that we can also order by the sales.
After sorting based off company, Within that particular company we do a second ordering based on sales column. 
- Notice the sales is now in ascending order for each individual in each company. Andrew with 100 and Zach with 300. Depends on the column order we provide in the syntax.

![paste-5be4bba474b5703aa2f4424ada5e7c76411e3bcf](https://user-images.githubusercontent.com/40534141/146930086-2eada02e-ca3e-49fc-83b4-63565acf54cd.jpg)

Example:
```sql
SELECT company,name,sales FROM table ORDER BY company,sales;
``` 