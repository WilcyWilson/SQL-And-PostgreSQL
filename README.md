### What are Databases?

- Databases are systems that allow users to store and organize data.
- They are useful when dealing with large amounts of data

### Who are the typical users that deal with Databases?

Analysts
- Marketing
- Business
- Sales
  
Technical
- Data Scientist
- Software Engineers
- Web Developers

### Difference between Excel Spreadsheets and Databases

Spreadsheets
- Used for One-time analysis
- Used if we quickly need to chart something out
- Reasonable data set size
- Ability for untrained people to work with data

Databases
- Maintains Data Integrity (Doesn't allow to simply change data just clicking on a table cell)
- Can handle massive amounts of data
- Quickly combine different datasets
- Automate steps for re-use
- Can support data for websites and applications

### What is SQL?

- SQL is a domain-specific language used in programming and designed for managing data held in a relational database management system, or for stream processing in a relational data stream management system.

### Setting up PostgreSQL and using DBeaver as SQL Client Software

- [Setting Up PostgreSQL in Arch Linux](https://github.com/WilcyWilson/Linux-Tips/tree/master/SettingUpPostgreSqlInArchLinux#readme)

- [Using DBeaver as SQL Client Software](https://github.com/WilcyWilson/Linux-Tips/tree/master/SettingUpMySqlInArchLinux#using-dbeaver-to-login-to-the-sql-server-through-gui)

- [Resolving DBeaver Issue](https://github.com/WilcyWilson/SQL-And-PostgreSQL/tree/master/IssuesWithDBeaverRestore#readme)

### SQL Syntax and Queries and What they do?

#### SELECT ..... FROM .....
- The SELECT syntax allows us to retrieve information from a table

Basic Sytax:
```sql
SELECT column_name FROM table_name
```

Example:
```sql
SELECT first_name,last_name,email,store_id FROM customer;
``` 

- As we can see we can retrieve multiple column names at once using SELECT.

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

#### SELECT ...... FROM ...... LIMIT .....
- LIMIT allows limit the number of rows returned for a query.
This is useful when we just want to view the layout of the table with top few rows.
- LIMIT also becomes useful in combination with ORDER BY statement. LIMIT goes very end of a query request and is the last command to be executed. Even after ORDER BY.

Example:
```sql
SELECT * FROM payment
WHERE amount != 0.00
ORDER BY payment_date desc
limit 5;
```

![paste-6faf414b44f78ca49a439c171382368707687c5c](https://user-images.githubusercontent.com/40534141/146930941-76ff8efa-e231-4cc4-b86d-b30e1e5a36dc.jpg)

#### SELECT ...... FROM ...... WHERE column BETWEEN value1 and value2
- BETWEEN keyword can be used to match a value against a range of values.
- Value between low and high are inclusive.
- We can combine BETWEEN with NOT logical operator, where we are asking for value not between the given values of low and high. NOT BETWEEN is the same as asking value<low or value > high. Exclusive of actual low point and high point.
- BETWEEN also includes time stamp information.

Example:
```sql
SELECT COUNT(*) from payment
WHERE amount NOT BETWEEN 8 and 9;
``` 

Things to note while using BETWEEN in a Date and Timestamp data
  
![paste-f30e4854df130beae3f4bd898e3986935ead0334](https://user-images.githubusercontent.com/40534141/147038785-81aa73dc-d323-4240-ae92-c0099574133f.jpg)
 
- These are the payment done between first of february of 2007 to 15th of february of 2007.
Notice the date format, year-month-day.
- These timestamp information includes both the date and hours/minutes etc.
- That means postgresql essentially has to decide to include time of 0000 hours or 24000 hours. So, when
we are dealing with inclusivity versus exclusitivity this actually affects our logic.
  
Why don't we get any data here?
  
![paste-719099c67dbf66dc217c4102c0c7e4002db61c26](https://user-images.githubusercontent.com/40534141/147038915-964e08b3-8eb0-4be7-a58c-d02916235e58.jpg)

- This is because. When we deal with this end date 2-14. It is only going up to the 0000 hours mark, its not going to the end which will be 24000 mark of the 14th. We have to double check when using between in a timestamp and date situation.

#### SELECT ...... FROM ...... WHERE column IN (value1,value2)
- We use IN operator to create a condition that checks to see if a value is included in a list of multiple options.
- Instead of having to write bunch of OR statement like name='David' or name='Jack'. We can use the IN operator to just create a condition to see if a value is included in the list of multiple options.
- We are specifying IN that anything that is red or blue will be returned to us.
Using NOT IN to exclude the values given.
  
![paste-2af0d2baaa8a32156bd620f67d978fe71e574a9a](https://user-images.githubusercontent.com/40534141/147042223-fe7ef451-a0bc-40dc-8daf-feb926d6ed4e.jpg)

Example:
```sql
SELECT * from payment
WHERE amount IN (0.99,1.98,1.99);
``` 

- Here it returns the data where amount is 0.99 or 1.98 or 1.99. Need to use WHERE to use IN.

