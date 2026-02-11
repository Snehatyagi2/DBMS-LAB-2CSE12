1# EXPERIMENT 3

## QUESTIONS WITH QUERIES

### 1. List all the employees and jobs in Department 30 in descending order by salary.
---
```sql
SELECT ENames , Jobs 
FROM EMPLOYEE
ORDER BY Sal DESC;
```
### 2. List job and department number of employees whose name are five letters long and began with "a" and end with "n".
```sql
SELECT Job, DeptNo 
FROM EMPLOYEE
WHERE EName LIKE "A___N";
```
### 3. Display the name of employees whose name start with alphabet s 
```sql
SELECT EName 
FROM EMPLOYEES
WHERE EName LIKE "S%"
```
### 4. Display the name of employees whose name end with alphabet s
```sql
SELECT EName 
FROM EMPLOYEES
WHERE EName LIKE "%S"
```
### 5. Display the names of employees working in department number 10 or 20 or 40 or employees working as clerks, salesman or analyst 
```sql
SELECT EName 
FROM EMPLOYEE
WHERE DeptNo IN (10,20,40)
OR
Job IN ("CLERK","SALESMAN","ANALYST");
```
### 6.Display employee number and names for employees who earn commission
```sql
 SELECT EmpNo, EName
FROM EMPLOYEE
WHERE Comm > 0;
```
### 7.Display employee number and total salary for each employee.
```sql
 SELECT EmpNo, (Sal + IFNULL (Comm,0))
AS "ANNUAL SALARY"
FROM EMPLOYEE;

```

### 8. Display employee number and annual salary for each employee.
```sql
 SELECT EmpNo, (Sal + IFNULL (Comm,0))
AS "ANNUAL SALARY"
FROM EMPLOYEE;
```
### 9. Display the names of all employees working as clerks and drawing a salary more than 3000.
```sql
SELECT EName 
FROM EMPLOYEE
WHERE Sal > 3000;
```
### 10. Display the names of all employees working as clerks, salesman or analyst drawing a salary more than 3000.
```sql
SELECT EName 
FROM EMPLOYEE
WHERE Job IN ("CLERK","SALESMAN","ANALYST")
AND Sal > 3000;
```

# END