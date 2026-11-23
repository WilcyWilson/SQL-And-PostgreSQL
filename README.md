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

</details>


## List of Contents

### [Introduction](https://github.com/WilcyWilson/SQL-And-PostgreSQL/tree/master/Introduction#readme)
### [SQL Statements Fundamentals](https://github.com/WilcyWilson/SQL-And-PostgreSQL/tree/master/SQLStatementsFundamentals#readme)
### [GROUP BY Statements](https://github.com/WilcyWilson/SQL-And-PostgreSQL/tree/master/GroupByStatements#readme)


