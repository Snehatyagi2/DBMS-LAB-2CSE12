# Experiment 5
---
## Question 1
##### Display
```sql
SELECT COUNT(*) FROM EMPLOYEE;
```
## Question 2
##### 
```sql
SELECT SUM(SAL) FROM EMPLOYEE;
```
## Question 3
##### 
```sql
 SELECT MAX(SAL) FROM EMPLOYEE;
```
## Question 4
##### 
```sql
SELECT AVG(SAL) FROM EMPLOYEE;
```
## Question 5
##### 
```sql
SELECT MAX(SAL) FROM EMPLOYEE
    -> WHERE Job IN ("CLERK");
```
## Question 6
##### 
```sql
 SELECT MAX(SAL) FROM EMPLOYEE
    -> WHERE DeptNo = 20;
```
## Question 7
##### 
```sql
SELECT MIN(SAL) FROM EMPLOYEE
    -> WHERE Job IN ("SALESMAN");
```
## Question 8
##### 
```sql
 SELECT MIN(SAL) FROM EMPLOYEE
    -> WHERE Job IN ("SALESMAN");
```
## Question 9
##### 
```sql
SELECT AVG(SAL) FROM EMPLOYEE
    -> WHERE Job IN ("MANAGER");
```
## Question 10
#####
```sql
SELECT SUM(SAL) FROM EMPLOYEE
    -> WHERE Job = "ANALYST"
    -> AND DeptNo = 40;
```
## Question 11
##### 
```sql
 SELECT UCASE(EName) FROM EMPLOYEE;
```
## Question 12
#####
```sql
 SELECT LCASE(EName) FROM EMPLOYEE;
```
## Question 13
##### 
```sql
 SELECT CONCAT(UPPER(LEFT(ENAME,1)),LOWER(SUBSTRING(EName,2)))
  AS PROPER_CASE FROM EMPLOYEE;
```
## Question 14
#####
```sql
SELECT LENGTH("SNEHA");
```
## Question 15
##### 
```sql
 SELECT ENAME,LENGTH(EName) 
FROM EMPLOYEE;
```


