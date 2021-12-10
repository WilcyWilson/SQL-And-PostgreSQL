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

- [Using DBeaver as SQL Client Software](https://github.com/WilcyWilson/Linux-Tips/tree/master/SettingUpPostgreSqlInArchLinux#readme)

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
