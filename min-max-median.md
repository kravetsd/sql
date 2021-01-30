## TASK
For this challenge you need to create a simple SELECT statement. Your task is to calculate the MIN, MEDIAN and MAX scores of the students from the results table.

### Tables:

#### Student
```
id
name
```

#### result
```
id
student_id
score
```

### resultant table:
min
median
max


---
## Answer
```
SELECT MIN(r.score),MAX(r.score),percentile_cont(0.5) WITHIN GROUP (ORDER BY score) as median
FROM result as r 
```
