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

