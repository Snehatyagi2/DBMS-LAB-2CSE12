# Experiment 7
---
## Question 1 - Days remaining in this year

```sql
SELECT DATEDIFF(CONCAT(YEAR(CURDATE()),'-12-31'), CURDATE()) AS days_left;
```
## Question 2 - Highest, lowest salary & difference
##### 
```sql
SELECT MAX(sal) AS highest,
MIN(sal) AS lowest,
MAX(sal)-MIN(sal) AS difference
FROM employee;
```
## Question 3 - Commission > 25% of salary
##### 
```sql
 SELECT * FROM employee
WHERE comm > sal*0.25;
```
## Question 4 - Salary in dollar format

##### 
```sql
SELECT CONCAT('$', FORMAT(sal,2)) FROM employee;
```
## Question 5 - Matrix query (job vs dept salary)
##### 
```sql
SELECT job,
SUM(CASE WHEN deptno=10 THEN sal END) AS dept10,
SUM(CASE WHEN deptno=20 THEN sal END) AS dept20,
SUM(CASE WHEN deptno=30 THEN sal END) AS dept30,
SUM(sal) AS total
FROM employee
GROUP BY job;
```
## Question 6 - Total employees hired in 1980–83
##### 
```sql
 SELECT COUNT(*) AS total,
SUM(CASE WHEN YEAR(hiredate)=1980 THEN 1 ELSE 0 END) AS y1980,
SUM(CASE WHEN YEAR(hiredate)=1981 THEN 1 ELSE 0 END) AS y1981,
SUM(CASE WHEN YEAR(hiredate)=1982 THEN 1 ELSE 0 END) AS y1982,
SUM(CASE WHEN YEAR(hiredate)=1983 THEN 1 ELSE 0 END) AS y1983
FROM employee;
```
## Question 7 - Last Sunday of current month
##### 
```sql
SELECT DATE_SUB(LAST_DAY(CURDATE()),
INTERVAL WEEKDAY(LAST_DAY(CURDATE()))+1 DAY);
```
## Question 8 - Dept number & total employees
##### 
```sql
 SELECT deptno, COUNT(*) 
FROM employee
GROUP BY deptno;
```
## Question 9 - Jobs & total employees
##### 
```sql
SELECT job, COUNT(*) 
FROM employee
GROUP BY job;
```
## Question 10 - Dept number & total salary
#####
```sql
SELECT deptno, SUM(sal)
FROM employee
GROUP BY deptno;
```


