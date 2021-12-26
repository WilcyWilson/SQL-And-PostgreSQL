#### What does GROUP BY do? 
- GROUP BY allows us to aggregate columns per some category.

#### Simple Example with Table:
- Let's imagine we have some columns in the table. Say Category represent company and data value.
- So, we have 10 dollar deal with company A and other 5 dollar deal with company A and so on.
- We need to first consider the category column. We need to choose a categorical column to GROUP BY.
- Categorical columns are non-continous. We are treating them as non continuous for the sake of GROUP BY.
- We need to keep in mind that these can still be numerical such as cabin class categories on a ship (eg. Class 1, Class 2).
- Columns appearing continuous can be treated as a category. Here, in dvdrental database we have rental rates like 9.99, 11.99 etc.
- We could treat these each rental rates as its own seperate class or category.
- So, when something is treated as categorical, it doesn't necessarily mean, its non numeric.

