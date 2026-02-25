# Experiment 6
---
## Question 1 
## Display empno, ename, deptno as department name

```sql
SELECT empno, ename,
CASE deptno
 WHEN 10 THEN 'ACCOUNTING'
 WHEN 20 THEN 'RESEARCH'
 WHEN 30 THEN 'SALES'
 WHEN 40 THEN 'OPERATIONS'
END AS dept_name
FROM employee;
```
## Question 2
## Display your age in days
##### 
```sql
SELECT DATEDIFF(CURDATE(), '2004-05-20') AS age_in_days;
```
## Question 3
## Display your age in months
##### 
```sql
 SELECT TIMESTAMPDIFF(MONTH, '2004-05-20', CURDATE()) AS age_in_months;
```
## Question 4
## Display current date as

## 15th August Friday Nineteen Ninety-Seven
##### 
```sql
SELECT DATE_FORMAT(CURDATE(), '%D %M %W %Y') AS formatted_date;
```
## Question 5
## Scott has joined the company on Wednesday 13th August 1990
##### 
```sql
SELECT CONCAT(ename,' has joined the company on ',
DATE_FORMAT(hiredate,'%W %D %M %Y'))
FROM employee
WHERE ename='SCOTT';
```
## Question 6
## Scott has joined the company on Wednesday 13th August 1990
##### 
```sql
 SELECT CONCAT(ename,' has joined the company on ',
DATE_FORMAT(hiredate,'%W %D %M %Y'))
FROM employee
WHERE ename='SCOTT';
```
## Question 7
## Nearest Saturday after current date
##### 
```sql
SELECT DATE_ADD(CURDATE(), INTERVAL (6 - WEEKDAY(CURDATE())) DAY) AS next_saturday;
```
## Question 8
## Display current time
##### 
```sql
 SELECT CURTIME();
```
## Question 9
## Date three months before current date
##### 
```sql
SELECT DATE_SUB(CURDATE(), INTERVAL 3 MONTH);
```
## Question 10
## Employees joined in December
#####
```sql
SELECT * FROM employee
WHERE MONTH(hiredate)=12;
```
## Question 11
## First 2 chars of hiredate = last 2 chars of salary
##### 
```sql
 SELECT * FROM employee
WHERE LEFT(DAY(hiredate),2) = RIGHT(sal,2);
```
## Question 12
## 10% of salary = year of joining
#####
```sql
 SELECT * FROM employee
WHERE sal*0.10 = YEAR(hiredate);
```
## Question 13
## Joined before 15th of month
##### 
```sql
 SELECT * FROM employee
WHERE DAY(hiredate) < 15;
```
## Question 14
## Joined before 15th of month
#####
```sql
SELECT * FROM employee
WHERE DAY(hiredate) < 15;
```
## Question 15
## Joining date available in deptno (not null)
##### 
```sql
 SELECT * FROM employee
WHERE hiredate IS NOT NULL;
```


