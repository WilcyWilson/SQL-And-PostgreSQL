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