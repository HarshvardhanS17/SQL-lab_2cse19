# Experiment 5

## AIM
To perform advanced SQL operations on the EMPLOYEE table including conditional retrieval using date and pattern matching conditions, filtering records using logical operators, calculating derived salary components (HRA, DA, PF, Total Salary), sorting records, and updating salary values based on specified conditions.

---

## Queries:

### Question 1
Display the list of employees who have joined the company before 30th June 80 or after 31st Dec 81.

```sql
SELECT * FROM EMPLOYEE WHERE HIREDATE < '1980-06-30' OR HIREDATE > '1981-12-31';
```

---

### Question 2
Display the names of employees whose names have second alphabet A in their names.

```sql
SELECT * FROM EMPLOYEE WHERE ENAME LIKE '_A%';
```

---

### Question 3
Display the names of employees whose name is exactly five
characters in length


```sql
SELECT empno,ename FROM employee WHERE ename LIKE '_____';
```

---

### Question 4
Display the names of employees whose names have second
alphabet A in their names.

```sql
SELECT * FROM EMPLOYEE WHERE ENAME LIKE '_A%';
```

---

### Question 5
Display the names of employees who are not working as salesman or clerk or analyst.

```sql
SELECT * FROM EMPLOYEE WHERE JOB NOT IN ('SALESMAN','CLERK','ANALYST');
```

---

### Question 6
Display the name of the employee along with their annual salary (sal*12). The name of the employee earning highest salary should appear first.

```sql
SELECT ename, sal*12 AS ANNUAL_SALARY FROM EMPLOYEE ORDER BY ANNUAL_SALARY DESC;
```

---

### Question 7
Display name, sal, hra, pf, da, totalsal for each employee. The output should be in the order of total sal, hra 15% of sal, da 10% of sal, pf 5% of sal. Total salary will be (sal*hra*da)-pf.

```sql
SELECT ename, sal, sal*0.15 AS hra, sal*0.10 AS da, sal*0.05 AS pf, (sal + sal*0.15 + sal*0.10 - sal*0.05) AS totalsal FROM EMPLOYEE;
```

---

### Question 8
Update the salary of each employee by 10% increment who are
not eligible for commission.

```sql
UPDATE EMPLOYEE SET SAL = SAL * 1.1 WHERE COMM IS NULL;
```

---

### Question 9
Display those employees whose salary is more than 3000 after
giving 20% increment.

```sql
SELECT * FROM EMPLOYEE WHERE SAL * 1.2 > 3000;
```

---

### Question 10
Display those employees whose salary contains atleast 3 digits

```sql
SELECT * FROM EMPLOYEE WHERE SAL >= 3;
```

---
