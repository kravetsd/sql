You will need to create SELECT statement in conjunction with LIKE.

Please list people which have first_name with at least 6 character long

##Names table schema
```
id
first_name
last_name
```
##Results table schema
```
first_name
last_name
```

---
##Code
```
-- Replace with your SQL Query
SELECT first_name,last_name
FROM names
WHERE first_name LIKE '______%'
```
