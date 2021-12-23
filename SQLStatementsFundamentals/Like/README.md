#### SELECT ...... FROM ...... WHERE column LIKE 'wildcard'
- The LIKE operator allows us to perform pattern matching against string data with the use of wildcard characters.

What are some wildcard characters of LIKE operator?
- Percent % --> Matches any sequence of characters.
- Underscore _ --> Matches any single character.

- All name that begins with A is WHERE name LIKE 'A%'
- All name that ends with a is WHERE name LIKE '%a'

Simple difference between LIKE and ILIKE?
- LIKE is case sensitive whereas ILIKE is not case sensitive.

Example
![paste-b4f99b84d57803f8bc65d94925e60ce5be0477bc](https://user-images.githubusercontent.com/40534141/147196476-33cf14f6-4413-4564-b8eb-9a13859e069f.jpg)

- Here first name starts with A but last name doesn't start with B and orders by last name.