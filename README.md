## Database Systems
<details>

<summary>
  <h2>Click to reveal.</h2>
</summary>


#### In a hierarchical database system, how is data represented?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      As one or more tree structures where nodes follow a single-parent hierarchy.
</details>

#### What is the defining characteristic of a network database system?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      It is a multiparent hierarchy where sets of links define relationships between different records.
</details>

#### Instead of using pointers to navigate between records, how does the relational model link entities?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      By using redundant data (foreign keys) stored in columns.
</details>

#### In a relational database, what is a primary key?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      A column (or set of columns) that uniquely identifies every row in a table.
</details>

#### What is a compound key?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      A primary key that consists of two or more columns.
</details>

#### What is the difference between a natural key and a surrogate key?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      A natural key is a primary key based on existing descriptive data; a surrogate key is a unique identifier generated specifically for the database.
</details>

#### Why is a cust_id (surrogate key) generally preferred over fname/lname (natural key)?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      Data like names can change, and primary key values should never change once assigned.
</details>

#### What is a foreign key?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      A column in one table that holds the primary key value of a record in a different table to create a relationship.
</details>

#### In relational database terminology, what is a join?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      The process of using a foreign key value to locate the corresponding row in another table.
</details>

#### What is the goal of normalization?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      Refining a database design to ensure that each independent piece of information is stored in exactly one place.
</details>

#### Why is it considered a violation of normalization to store a customer's name in an account table that already has a cust_id?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      It creates redundant data; if the name changes, it must be updated in multiple places, leading to potential data unreliability.
</details>

#### What is a compound key?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      A primary key that is composed of two or more columns.
</details>

#### True or False: A primary key value can be updated once it has been assigned.
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      False; primary key columns should never be allowed to change once a value has been assigned.
</details>

#### How are foreign keys represented in the relational model?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      As redundant data columns that refer to the primary key of another table.
</details>

#### In the context of data management, what is the simplest definition of a database?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      A set of related information.
</details>

#### Why is finding a name based on a specific address "impractical" in a standard physical telephone book?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      The database is indexed only by names, not by addresses.
</details>

#### Why does the accuracy of a printed paper database inevitably decline over time?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      It cannot reflect real-time changes, such as people moving or changing contact details.
</details>

#### What is a database system?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      A computerized mechanism for data storage and retrieval.
</details>

#### Identify three primary advantages of electronic database systems over paper-based systems.
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      1. Faster retrieval
      2. Multiple indexing methods
      3. Up-to-the-minute information.
</details>

#### In early tape-based systems, why did multiple requests for the same data often require multiple physical reads?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      The computers had very little memory (RAM) to store or cache the data.
</details>

#### How do modern database systems achieve high-speed access to petabytes of data?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      They use clusters of servers to cache large amounts of data in high-speed memory.
</details>

#### What specific advantage does electronic indexing provide over the fixed indexing of a physical book?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      Electronic systems can index data in multiple ways, allowing for various search criteria.
</details>

#### In database design, what is an entity?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      Something of interest to the database user community, such as customers, parts, or geographic locations.
</details>

#### What is a column in the context of a relational database?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      An individual piece of data stored in a table.
</details>

#### What is a row (also known as a record)?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      A set of columns that together completely describe an entity or some action on an entity.
</details>

#### What is the formal definition of a table?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      A set of rows held either in memory (nonpersistent) or on permanent storage (persistent).
</details>

#### What is a result set?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      Another name for a nonpersistent table, generally created as the output of an SQL query.
</details>

#### What is the specific purpose of a primary key?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      One or more columns used as a unique identifier for each row in a table.
</details>

#### What is the specific purpose of a foreign key?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      One or more columns used together to identify a single row in another table.
</details>

#### What was the original name of the language that eventually became SQL?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      SEQUEL (derived from SQUARE and DSL/Alpha).
</details>

#### Is SQL technically an acronym for "Structured Query Language"?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      No; although commonly used that way, the official name is simply the letters S. Q. L.
</details>

#### What is the defining characteristic of a nonprocedural language like SQL?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      You define the desired results, but the process (mechanism) of how to generate them is left to an external agent.
</details>

#### In a database engine, what component decides the most efficient execution path for a query?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      The optimizer.
</details>

#### What is the purpose of SQL schema statements (DDL) Data Definition Language?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      To define and manage the data structures (e.g., tables) stored in the database.
</details>

#### What is the purpose of SQL data statements (DML)?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      To manipulate (retrieve or modify) the data within previously defined structures.
</details>

#### What is the purpose of SQL transaction statements?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      To begin, end, and roll back transactions.
</details>

#### What is metadata in the context of a database?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      Data about the database itself, such as the names of tables and columns.
</details>

#### Where does a database store metadata?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      In the data dictionary (a special set of internal tables).
</details>

#### How can a developer dynamically determine the current set of columns in a table at runtime?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      By using a SELECT statement to query the data dictionary.
      select column_name from information_schema.columns;
</details>

#### What is the standard syntax for multi-line comments in most SQL implementations?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      Text enclosed between /* and */.
</details>

#### In a standard SQL query, what is the specific role of the FROM clause?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      To determine which table or tables will be used as the data source.
</details>

#### In a standard SQL query, what is the specific role of the WHERE clause?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      To filter out data rows that do not meet specific conditions.
</details>

#### What is the architectural result of an SQL query?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      A result set (which is effectively a nonpersistent table).
</details>

#### What happens if you execute a DELETE or UPDATE statement without a WHERE clause?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
      The operation will affect every row in the table.
</details>

#### Write a MySQL statement to create a table corp with a SMALLINT ID (Primary Key) and a VARCHAR(30) name.
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
    CREATE TABLE corp (
    corp_id SMALLINT,
    name VARCHAR(30),
    PRIMARY KEY (corp_id)
    );
</details>

#### Write a MySQL statement to modify the name column of a product to 'Gold' where the product_id is 5.
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
    UPDATE product
    SET name = 'Gold'
    WHERE product_id = 5;
</details>

#### What is the standard toolkit used to execute SQL statements from a Java application?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
    JDBC (Java Database Connectivity).
</details>

#### What is the standard toolkit used to execute SQL statements from a C# (.NET) application?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
    ADO.NET.

  <img width="930" height="80" alt="image" src="https://github.com/user-attachments/assets/5a02b78e-6401-4297-bffc-b688681aa4b6" />

</details>

#### Why do database engines provide optimizer hints?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
    To allow developers to influence or override the optimizer's choice of execution path (e.g., forcing a specific index).
</details>

#### Write the command to log into the mysql command-line tool as the user root.
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
    mysql -u root -p;
</details>

#### Write the command to log into the mysql command-line tool as root while immediately selecting the sakila database.
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
    mysql -u root -p sakila;
</details>

#### In the mysql command-line tool, what command displays a list of all available databases?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
    SHOW DATABASES;
</details>

#### In the mysql command-line tool, what command sets the active database for subsequent queries?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
    USE [database_name];
</details>

#### Write a MySQL query to retrieve the current date and time.
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
    SELECT now();
</details>

#### What is the purpose of the dual table in MySQL?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
    To provide compatibility with database engines (like Oracle) that require a FROM clause even when calling functions.
</details>

#### How do you execute an external SQL script file from within the mysql command-line tool?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
    Use the SOURCE command followed by the file path (e.g., SOURCE C:\temp\script.sql;).
</details>

#### What is Apache Drill?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
    An open-source query engine that allows users to write SQL queries to access data stored across diverse systems like Hadoop, NoSQL, JSON, and CSV.
</details>

#### What are the two standard commands used to close a mysql command-line session?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
    quit; and exit;
</details>

#### When installing the Sakila sample database, which file must be sourced first: the schema file or the data file?
<details>
  <summary>
    Click to reveal answer.
  </summary>
  
    The schema file (to create the table structures before populating them).
</details>

</details>


## List of Contents

### [Introduction](https://github.com/WilcyWilson/SQL-And-PostgreSQL/tree/master/Introduction#readme)
### [SQL Statements Fundamentals](https://github.com/WilcyWilson/SQL-And-PostgreSQL/tree/master/SQLStatementsFundamentals#readme)
### [GROUP BY Statements](https://github.com/WilcyWilson/SQL-And-PostgreSQL/tree/master/GroupByStatements#readme)


