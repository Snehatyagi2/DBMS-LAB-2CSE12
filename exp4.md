# Experiment 4
---
## Question 1
##### Display the list of employees who have joined the company before 30th june 80 or after 31st Dec 81.
```sql
SELECT *
FROM emp
WHERE hiredate < '30-JUN-80'
   OR hiredate > '31-DEC-81';
```
## Question 2
##### Display the names of employees whose names have second alphabet A in their names.
```sql
SELECT ename
FROM emp
WHERE ename LIKE '_A%';
```
## Question 3
##### Display the names of employees whose name is exactly five letters in length.
```sql
SELECT ename
FROM emp
WHERE LENGTH(ename) = 5;
```
## Question 4
##### Display the name of employees whose names have last alphabet A in their names.
```sql
SELECT ename
FROM emp
WHERE ename LIKE 'A%';
```
## Question 5
##### Display the names of employees who are not working as salesman or clerk or analyst.
```sql
SELECT ename, job
FROM emp
WHERE job NOT IN ('SALESMAN', 'CLERK', 'ANALYST');
```
## Question 6
##### Display the name of the employee along with their annual salary (sal * 12). The name of the employee earning highest salary should appear first.
```sql
SELECT ename, sal*12 AS annual_salary
FROM emp
ORDER BY sal DESC;
```
## Question 7
##### Display name, sal, hra, pf, da, totalsal for each employee.The output should be in the order of total sal.hra = 15% of sal,da = 10% of sal,pf = 5% of sal.Total salary will be (sal + hra + da) − pf. 
```sql
SELECT ename,
       sal,
       sal*0.15 AS hra,
       sal*0.10 AS da,
       sal*0.05 AS pf,
       (sal + sal*0.15 + sal*0.10 - sal*0.05) AS totalsal
FROM emp
ORDER BY totalsal;
```
## Question 8
##### Update the salary of each employee by 10% increment who are not eligible for commission.
```sql
UPDATE emp
SET sal = sal * 1.10
WHERE comm IS NULL;
```
## Question 9
##### Display those employees whose salary is more than 3000 after giving 20% increment.
```sql
SELECT ename, sal, sal*1.20 AS incremented_salary
FROM emp
WHERE sal*1.20 > 3000;
```
## Question 10
##### Display those employees whose salary contains at least 3 digits.
```sql
SELECT ename, sal
FROM emp
WHERE LENGTH(sal) >= 3;
```

