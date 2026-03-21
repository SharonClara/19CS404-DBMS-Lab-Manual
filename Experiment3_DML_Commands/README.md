# Experiment 3: DML Commands

## AIM
To study and implement DML (Data Manipulation Language) commands.

## THEORY

### 1. INSERT INTO
Used to add records into a relation.
These are three type of INSERT INTO queries which are as
A)Inserting a single record
**Syntax (Single Row):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES (value_1, value_2, ...);
```
**Syntax (Multiple Rows):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES
(value_1, value_2, ...),
(value_3, value_4, ...);
```
**Syntax (Insert from another table):**
```sql
INSERT INTO table_name SELECT * FROM other_table WHERE condition;
```
### 2. UPDATE
Used to modify records in a relation.
Syntax:
```sql
UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
```
### 3. DELETE
Used to delete records from a relation.
**Syntax (All rows):**
```sql
DELETE FROM table_name;
```
**Syntax (Specific condition):**
```sql
DELETE FROM table_name WHERE condition;
```
### 4. SELECT
Used to retrieve records from a table.
**Syntax:**
```sql
SELECT column1, column2 FROM table_name WHERE condition;
```
**Question 1**
--
Write a SQL statement to increase the salary of employees under the department 40, 90 and 110 according to the company rules. Salary will be increased by 25% for the department 40, 15% for department 90 and 10% for the department 110 and the rest of the departments will remain same.
```sql
update Employees
set salary=
    case
        when department_id=40 then round(salary*1.25 )
        when department_id=90 then round(salary*1.15 )
        when department_id=110 then round(salary*1.1 )
        else salary
    end;
```

**Output:**
<img width="1173" height="265" alt="515536829-8f8857bd-ab5c-431e-9d55-75cd38374296" src="https://github.com/user-attachments/assets/23e7b1f7-f07b-4c0a-bd12-c38a59f676dc" />



**Question 2**
---

Write a SQL statement to double the availability of the product with product_id 1.
```sql

update products
set availability=2*availability
where product_id=1;
```

**Output:**

<img width="976" height="220" alt="515537045-d2426339-e40e-4f94-a491-7d2fa574b18c" src="https://github.com/user-attachments/assets/731f2f07-a8d4-45bf-ba88-6644d7fe3693" />


**Question 3**
---
Write a SQL statement to Increase the selling price by 15% in the products table where quantity in stock is less than 50 and supplier ID is 10.
```sql
update Products
set sell_price=sell_price*1.15
where quantity<50 and  supplier_id=10;
```

**Output:**

<img width="1220" height="293" alt="515537284-4733d570-98bb-45b4-8553-5c4100bc8d0c" src="https://github.com/user-attachments/assets/ba5398ac-3eb1-4486-a40a-a80222a9f1a2" />


**Question 4**
---
Write a SQL statement to Update the product_name to 'Premium Bread' whose product ID is 5 in the products table.
```sql
update Products
set product_name='Premium Bread'
where product_id=5;
```

**Output:**

<img width="1181" height="233" alt="515537478-93a6655c-1adc-4055-9732-81844553bf7a" src="https://github.com/user-attachments/assets/d7a6ce3f-0d79-4bcb-ad45-00c67fe2210a" />


**Question 5**
---
Change the supplier name to upper case where contact person contains ' Singh' in suppliers table.

```sql
update suppliers
set supplier_name=upper(supplier_name) 
where contact_person like '%Singh';
```

**Output:**
<img width="1362" height="231" alt="515537796-c464446d-601e-48ce-9a47-b4ff9a602bcb" src="https://github.com/user-attachments/assets/ad819efb-0a3e-42c0-856a-b5a9cc11fc67" />


**Question 6**
---

Write a SQL query to Delete customers with 'GRADE' 3 and whose 'CUST_NAME' contains the substring 'BBB', and 'PAYMENT_AMT' is greater than 2000

```sql
delete from customer
where grade=3 and cust_name like "%BBB%" and PAYMENT_AMT>2000;
```

**Output:**
<img width="1358" height="302" alt="515538006-e4195b9c-b253-4740-8bd4-9dce7c11b08d" src="https://github.com/user-attachments/assets/5c9a4a6c-09cc-44e6-9928-373c5dfb6547" />



**Question 7**
---

Write a SQL query to Delete a Specific Surgery whose ID is 3

```sql
delete from Surgeries
where surgery_id=3;

```

**Output:**

<img width="655" height="233" alt="515538373-a1027702-d148-4bb1-90c7-a8abe3f5b82b" src="https://github.com/user-attachments/assets/b2a522ca-21a2-4e2d-a6a3-e104fb01e6e4" />


**Question 8**
---

Write a SQL query to delete a specific doctor from Doctors table whose ID is 1.

```sql
delete from doctors
where doctor_id=1;

```

**Output:**
<img width="710" height="172" alt="515538725-139b1f93-df1f-447d-9680-cd71f61927a1" src="https://github.com/user-attachments/assets/71760ada-17ed-4aef-ab37-e3d94cdc9c4b" />


**Question 9**
---
Write a SQL query to Delete customers whose 'GRADE' is greater than 2 and have a 'PAYMENT_AMT' less than the average 'PAYMENT_AMT' for all customers, or whose 'OUTSTANDING_AMT' is greater than 8000.

```sql

delete from customer
where grade>2 and payment_amt<(select avg(payment_amt) from customer) or outstanding_amt>8000;
```

**Output:**

<img width="1448" height="339" alt="515539442-f210b08c-8741-4fb0-9612-b16c81d5b6fd" src="https://github.com/user-attachments/assets/d420d392-1f47-4867-b317-3b0b3e095f1f" />


**Question 10**
---

Write a SQL query to Delete All Doctors with a NULL Specialization

```sql
delete from doctors
where specialization is null;

```

**Output:**
<img width="609" height="517" alt="515539665-cde49bf8-0eeb-428a-bc06-133b060b1c47" src="https://github.com/user-attachments/assets/d4f86d6b-748d-48d5-87c4-33caaa5e0995" />


## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
