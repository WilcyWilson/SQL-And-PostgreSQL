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



