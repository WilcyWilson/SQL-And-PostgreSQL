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