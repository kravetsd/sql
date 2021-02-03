## Task:
For this challenge you need to create a SELECT statement, this SELECT statement will use an IN to check whether a department has had a sale with a price over 90.00 dollars BUT the sql MUST use the WITH statement which will be used to select all columns from `sales` where the price is greater than 90.00, you must call this sub-query `special_sales`.

### Departments table schema
```
id
name
```

### Sales table schema
```
id
department_id (department foreign key)
name
price
card_name
card_number
transaction_date
```

### Resultant table schema
```
id
name
```

---

## Resulting query:

```
WITH special_sales AS (
  SELECT department_id
  FROM sales
  WHERE price > 90.00
)
SELECT id,name
FROM departments
WHERE id in (SELECT * FROM special_sales)
```