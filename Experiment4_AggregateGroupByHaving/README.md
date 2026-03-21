# Experiment 4: Aggregate Functions, Group By and Having Clause

## AIM
To study and implement aggregate functions, GROUP BY, and HAVING clause with suitable examples.

## THEORY

### Aggregate Functions
These perform calculations on a set of values and return a single value.

- **MIN()** – Smallest value  
- **MAX()** – Largest value  
- **COUNT()** – Number of rows  
- **SUM()** – Total of values  
- **AVG()** – Average of values

**Syntax:**
```sql
SELECT AGG_FUNC(column_name) FROM table_name WHERE condition;
```
### GROUP BY
Groups records with the same values in specified columns.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name;
```
### HAVING
Filters the grouped records based on aggregate conditions.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name
HAVING condition;
```

**Question 1**
---

What is the average dosage prescribed for each medication?

```sql
select medication,avg(dosage) as AvgDosage 
from Prescriptions 
group by medication;

```

**Output:**
<img width="629" height="827" alt="515541507-40c40750-4b29-4673-88ca-1a3a6653895a" src="https://github.com/user-attachments/assets/45b47c19-06f2-44ff-80fe-f91c1ab153b0" />


**Question 2**
---

How many prescriptions were written in each frequency category (e.g., once daily, twice daily)?

```sql
select frequency,count(PrescriptionID) as TotalPrescriptions
from Prescriptions
group by frequency;

```

**Output:**
<img width="758" height="598" alt="515541642-c7ca3265-b9f4-45da-b2ac-259a6619d661" src="https://github.com/user-attachments/assets/2122a305-ad71-4968-85b8-156b59c253c6" />


**Question 3**
---

How many medical records are there for each patient?

```sql
select PatientID,count(RecordID) as TotalRecords
from MedicalRecords
group by PatientID;

```

**Output:**
<img width="597" height="732" alt="515541792-bfec625f-c690-47ef-b291-dbd83e192bec" src="https://github.com/user-attachments/assets/9948bede-9735-4c8e-8a10-7e3f7a15bee1" />



**Question 4**
---

Write a SQL query to return the total number of rows in the 'customer' table where the city is not Noida.

```sql
select count(*) as COUNT from customer
where city != "Noida";
```

**Output:**

<img width="382" height="397" alt="515542007-564562d1-cae9-451c-bea7-729f6d4d3da1" src="https://github.com/user-attachments/assets/f3959d2f-6dcd-4bdc-b3b9-a17a00b50474" />


**Question 5**
---

Write a SQL query to calculate total purchase amount of all orders. Return total purchase amount.
```sql

select sum(purch_amt) as TOTAL from orders;

```

**Output:**
<img width="356" height="377" alt="515542165-6758f8c0-f24f-4c63-b400-d9c76cbf8c93" src="https://github.com/user-attachments/assets/eca04f11-3ffa-42a2-946d-676be9d5efa3" />


**Question 6**
---

Write a SQL query to Calculate the average income of the employees with names starting with 'A':

```sql
select avg(income) as avg_income from employee
where name like "A%";

```

**Output:**
<img width="368" height="377" alt="515542332-5cc2ae59-ce63-48b5-956c-7bc5d741982e" src="https://github.com/user-attachments/assets/245a3e8e-5557-4ff7-b3c5-c7298c93af1b" />



**Question 7**
---

Write a SQL query to calculate the average purchase amount of all orders. Return average purchase

```sql

select avg(purch_amt) as AVERAGE from orders;

```

**Output:**

<img width="352" height="380" alt="515542507-c79eaaf7-4ef1-443e-93eb-dbc8433c7de5" src="https://github.com/user-attachments/assets/3a54c028-04b3-4f45-8664-53058df2417e" />


**Question 8**
---

Write the SQL query that achieves the grouping of data by city, calculates the average income for each city, and includes only those cities where the average income is greater than 500,000.
```sql

select city,AVG(income)
from employee
group by city
having avg(income)>500000;
```

**Output:**
<img width="607" height="508" alt="515542656-b8daadd4-7657-4d02-821b-ab42c904a836" src="https://github.com/user-attachments/assets/f97dd58a-9851-4ff2-af8d-38dca61600e4" />



**Question 9**
---

Write the SQL query that achieves the grouping of data by age, calculates the minimum income for each age group, and includes only those age groups where the minimum income is less than 400,000.

```sql
select age,MIN(income) from employee
group by age
having min(income)<400000;
```

**Output:**

<img width="581" height="451" alt="515542835-4bb149ea-e51f-4279-b059-f93f7d8ea466" src="https://github.com/user-attachments/assets/fb04178d-ed8f-485a-b888-1cc03a25756b" />


**Question 10**
---

Write the SQL query that accomplishes the selection of product which has lowest price in each category from the "products" table and includes only those products where the minimum price is less than 10.
```sql
select category_id,min(price) as Price from products
group by category_id
having min(price)<10;

```

**Output:**
<img width="653" height="454" alt="515543005-c52deba0-d093-4409-add0-8a776e8d3325" src="https://github.com/user-attachments/assets/4d843e2d-8c11-4ffc-800b-9601053b4d58" />



## RESULT
Thus, the SQL queries to implement aggregate functions, GROUP BY, and HAVING clause have been executed successfully.
