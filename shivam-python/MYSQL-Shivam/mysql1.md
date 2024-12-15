### 🔥 **Complete List of SQL Commands**

SQL commands are grouped into several categories based on their functionality: **DDL**, **DML**, **DQL**, **DCL**, **TCL**, and **Utility Commands**. Below is a categorized list with explanations and examples.

---

### 1️⃣ **DDL (Data Definition Language)**

These commands are used to define, modify, and manage the structure of database objects like tables, schemas, and indexes.

| **Command**       | **Description**                                   | **Example**                                                               |
|--------------------|---------------------------------------------------|---------------------------------------------------------------------------|
| **`CREATE`**      | Creates a new table, database, or object.         | `CREATE TABLE employees (id INT, name VARCHAR(50));`                     |
| **`ALTER`**       | Modifies the structure of an existing table.      | `ALTER TABLE employees ADD age INT;`                                     |
| **`DROP`**        | Deletes an object like a table or database.       | `DROP TABLE employees;`                                                  |
| **`TRUNCATE`**    | Removes all rows from a table (cannot be rolled back). | `TRUNCATE TABLE employees;`                                              |
| **`RENAME`**      | Renames an object like a table.                   | `RENAME TABLE employees TO staff;`                                       |

---

### 2️⃣ **DML (Data Manipulation Language)**

These commands deal with the manipulation of data within tables.

| **Command**       | **Description**                                   | **Example**                                                               |
|--------------------|---------------------------------------------------|---------------------------------------------------------------------------|
| **`INSERT`**      | Adds new rows to a table.                         | `INSERT INTO employees (id, name) VALUES (1, 'Alice');`                  |
| **`UPDATE`**      | Modifies existing rows in a table.                | `UPDATE employees SET name = 'Bob' WHERE id = 1;`                        |
| **`DELETE`**      | Removes specific rows from a table.               | `DELETE FROM employees WHERE id = 1;`                                    |

---

### 3️⃣ **DQL (Data Query Language)**

This command is used to query data from tables.

| **Command**       | **Description**                                   | **Example**                                                               |
|--------------------|---------------------------------------------------|---------------------------------------------------------------------------|
| **`SELECT`**      | Retrieves data from a table.                      | `SELECT * FROM employees;`                                               |

---

### 4️⃣ **DCL (Data Control Language)**

These commands deal with access control and permissions.

| **Command**       | **Description**                                   | **Example**                                                               |
|--------------------|---------------------------------------------------|---------------------------------------------------------------------------|
| **`GRANT`**       | Grants permissions to users.                      | `GRANT SELECT ON employees TO user1;`                                    |
| **`REVOKE`**      | Removes previously granted permissions.           | `REVOKE SELECT ON employees FROM user1;`                                 |

---

### 5️⃣ **TCL (Transaction Control Language)**

These commands manage transactions in a database.

| **Command**       | **Description**                                   | **Example**                                                               |
|--------------------|---------------------------------------------------|---------------------------------------------------------------------------|
| **`START TRANSACTION`** | Begins a transaction.                        | `START TRANSACTION;`                                                     |
| **`COMMIT`**      | Saves changes made in a transaction.              | `COMMIT;`                                                                |
| **`ROLLBACK`**    | Reverts changes made in a transaction.            | `ROLLBACK;`                                                              |
| **`SAVEPOINT`**   | Sets a point within a transaction.                | `SAVEPOINT sp1;`                                                         |
| **`RELEASE SAVEPOINT`** | Deletes a savepoint.                         | `RELEASE SAVEPOINT sp1;`                                                 |
| **`SET TRANSACTION`** | Configures transaction properties.             | `SET TRANSACTION READ ONLY;`                                             |

---

### 6️⃣ **Utility Commands**

These commands help manage databases, users, and other database-level settings.

| **Command**       | **Description**                                   | **Example**                                                               |
|--------------------|---------------------------------------------------|---------------------------------------------------------------------------|
| **`USE`**         | Selects a database to use.                        | `USE company;`                                                           |
| **`SHOW`**        | Displays database objects or settings.            | `SHOW TABLES;`, `SHOW DATABASES;`, `SHOW GRANTS FOR user1;`              |
| **`DESCRIBE`** or **`DESC`** | Describes the structure of a table.            | `DESCRIBE employees;`                                                    |
| **`EXPLAIN`**     | Shows query execution details (for optimization). | `EXPLAIN SELECT * FROM employees;`                                       |

---

### 7️⃣ **Other SQL Commands**

#### Indexes
| **Command**       | **Description**                                   | **Example**                                                               |
|--------------------|---------------------------------------------------|---------------------------------------------------------------------------|
| **`CREATE INDEX`**| Creates an index for faster querying.             | `CREATE INDEX idx_name ON employees(name);`                               |
| **`DROP INDEX`**  | Deletes an index.                                 | `DROP INDEX idx_name ON employees;`                                       |

#### Views
| **Command**       | **Description**                                   | **Example**                                                               |
|--------------------|---------------------------------------------------|---------------------------------------------------------------------------|
| **`CREATE VIEW`** | Creates a virtual table (view).                   | `CREATE VIEW high_salary AS SELECT * FROM employees WHERE salary > 50000;`|
| **`DROP VIEW`**   | Deletes a view.                                   | `DROP VIEW high_salary;`                                                 |

#### Stored Procedures
| **Command**       | **Description**                                   | **Example**                                                               |
|--------------------|---------------------------------------------------|---------------------------------------------------------------------------|
| **`CREATE PROCEDURE`** | Creates a stored procedure.                   | ```sql CREATE PROCEDURE GetEmployees() SELECT * FROM employees; ```       |
| **`CALL`**        | Executes a stored procedure.                      | `CALL GetEmployees();`                                                   |
| **`DROP PROCEDURE`** | Deletes a stored procedure.                     | `DROP PROCEDURE GetEmployees;`                                           |

#### Functions
| **Command**       | **Description**                                   | **Example**                                                               |
|--------------------|---------------------------------------------------|---------------------------------------------------------------------------|
| **`CREATE FUNCTION`** | Creates a function.                             | ```sql CREATE FUNCTION TotalSalary() RETURNS DECIMAL(10,2) BEGIN RETURN (SELECT SUM(salary) FROM employees); END; ``` |
| **`DROP FUNCTION`** | Deletes a function.                              | `DROP FUNCTION TotalSalary;`                                             |

#### Triggers
| **Command**       | **Description**                                   | **Example**                                                               |
|--------------------|---------------------------------------------------|---------------------------------------------------------------------------|
| **`CREATE TRIGGER`** | Creates a trigger that executes before/after a DML operation. | ```sql CREATE TRIGGER before_update BEFORE UPDATE ON employees FOR EACH ROW BEGIN SET NEW.updated_at = NOW(); END; ``` |
| **`DROP TRIGGER`**  | Deletes a trigger.                               | `DROP TRIGGER before_update;`                                            |

---

### 🔥 **Summary of SQL Commands**

| **Category**          | **Commands**                                                                                                   |
|-----------------------|---------------------------------------------------------------------------------------------------------------|
| **DDL**               | `CREATE`, `ALTER`, `DROP`, `TRUNCATE`, `RENAME`                                                              |
| **DML**               | `INSERT`, `UPDATE`, `DELETE`                                                                                 |
| **DQL**               | `SELECT`                                                                                                     |
| **DCL**               | `GRANT`, `REVOKE`                                                                                            |
| **TCL**               | `START TRANSACTION`, `COMMIT`, `ROLLBACK`, `SAVEPOINT`, `SET TRANSACTION`                                     |
| **Utility**           | `USE`, `SHOW`, `DESCRIBE`, `EXPLAIN`                                                                         |
| **Indexes**           | `CREATE INDEX`, `DROP INDEX`                                                                                 |
| **Views**             | `CREATE VIEW`, `DROP VIEW`                                                                                   |
| **Stored Procedures** | `CREATE PROCEDURE`, `CALL`, `DROP PROCEDURE`                                                                 |
| **Functions**         | `CREATE FUNCTION`, `DROP FUNCTION`                                                                           |
| **Triggers**          | `CREATE TRIGGER`, `DROP TRIGGER`                                                                             |

****



Here’s a detailed explanation of **MySQL queries with table examples**. I’ll create a sample table and demonstrate queries on it for better understanding.

---

### Sample Table: **`employees`**

```sql
CREATE TABLE employees (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    age INT,
    department VARCHAR(50),
    salary DECIMAL(10, 2),
    joining_date DATE
);

-- Insert sample data
INSERT INTO employees (name, age, department, salary, joining_date)
VALUES 
('Alice', 30, 'HR', 60000, '2020-01-15'),
('Bob', 45, 'Finance', 75000, '2018-07-23'),
('Charlie', 25, 'IT', 50000, '2021-06-30'),
('Diana', 35, 'HR', 65000, '2019-03-10'),
('Ethan', 50, 'Finance', 80000, '2015-09-01');
```

**`employees` Table:**
| **id** | **name**   | **age** | **department** | **salary** | **joining_date** |
|--------|------------|---------|----------------|------------|------------------|
| 1      | Alice      | 30      | HR             | 60000.00   | 2020-01-15       |
| 2      | Bob        | 45      | Finance        | 75000.00   | 2018-07-23       |
| 3      | Charlie    | 25      | IT             | 50000.00   | 2021-06-30       |
| 4      | Diana      | 35      | HR             | 65000.00   | 2019-03-10       |
| 5      | Ethan      | 50      | Finance        | 80000.00   | 2015-09-01       |

---

### 1️⃣ **Basic Queries**

#### Select All Rows
```sql
SELECT * FROM employees;
```
**Result:**
Displays all rows and columns from the `employees` table.

---

#### Select Specific Columns
```sql
SELECT name, salary FROM employees;
```
**Result:**
| **name**   | **salary** |
|------------|------------|
| Alice      | 60000.00   |
| Bob        | 75000.00   |
| Charlie    | 50000.00   |
| Diana      | 65000.00   |
| Ethan      | 80000.00   |

---

#### Insert Data
```sql
INSERT INTO employees (name, age, department, salary, joining_date)
VALUES ('Frank', 28, 'IT', 55000, '2022-05-01');
```
**Result:** A new row is added to the `employees` table.

---

#### Update Data
```sql
UPDATE employees 
SET salary = 70000 
WHERE name = 'Charlie';
```
**Result:** Updates Charlie’s salary to 70000.

---

#### Delete Data
```sql
DELETE FROM employees 
WHERE age > 50;
```
**Result:** Deletes employees older than 50.

---

### 2️⃣ **Filtering Data**

#### Using `WHERE` Clause
```sql
SELECT * FROM employees WHERE department = 'HR';
```
**Result:**
| **id** | **name** | **age** | **department** | **salary** | **joining_date** |
|--------|----------|---------|----------------|------------|------------------|
| 1      | Alice    | 30      | HR             | 60000.00   | 2020-01-15       |
| 4      | Diana    | 35      | HR             | 65000.00   | 2019-03-10       |

---

#### Using `BETWEEN`
```sql
SELECT name, salary FROM employees WHERE salary BETWEEN 60000 AND 80000;
```
**Result:**
| **name**   | **salary** |
|------------|------------|
| Alice      | 60000.00   |
| Bob        | 75000.00   |
| Diana      | 65000.00   |

---

#### Using `LIKE`
```sql
SELECT * FROM employees WHERE name LIKE 'A%';
```
**Result:** Finds names starting with 'A' (e.g., Alice).

---

### 3️⃣ **Sorting and Limiting Results**

#### Sorting (`ORDER BY`)
```sql
SELECT * FROM employees ORDER BY salary DESC;
```
**Result:** Displays employees sorted by salary in descending order.

---

#### Limiting Results (`LIMIT`)
```sql
SELECT * FROM employees ORDER BY age ASC LIMIT 3;
```
**Result:** Displays the 3 youngest employees.

---

### 4️⃣ **Aggregate Functions**

#### Total Salary (`SUM`)
```sql
SELECT SUM(salary) AS total_salary FROM employees;
```
**Result:**
| **total_salary** |
|------------------|
| 330000.00        |

---

#### Average Salary (`AVG`)
```sql
SELECT AVG(salary) AS average_salary FROM employees;
```
**Result:**
| **average_salary** |
|--------------------|
| 66000.00           |

---

#### Count Employees (`COUNT`)
```sql
SELECT COUNT(*) AS total_employees FROM employees;
```
**Result:**
| **total_employees** |
|---------------------|
| 5                   |

---

### 5️⃣ **Grouping and Filtering Groups**

#### Group by Department
```sql
SELECT department, COUNT(*) AS employee_count FROM employees GROUP BY department;
```
**Result:**
| **department** | **employee_count** |
|----------------|---------------------|
| HR             | 2                  |
| Finance        | 2                  |
| IT             | 1                  |

---

#### Using `HAVING`
```sql
SELECT department, AVG(salary) AS avg_salary 
FROM employees 
GROUP BY department 
HAVING avg_salary > 60000;
```
**Result:**
| **department** | **avg_salary** |
|----------------|----------------|
| HR             | 62500.00       |
| Finance        | 77500.00       |

---

### 6️⃣ **Joining Tables**

#### Sample Tables

**`departments` Table:**
| **id** | **name**      |
|--------|---------------|
| 1      | HR            |
| 2      | Finance       |
| 3      | IT            |

---

#### Inner Join
```sql
SELECT employees.name, departments.name AS department_name
FROM employees
INNER JOIN departments ON employees.department = departments.name;
```
**Result:**
| **name**   | **department_name** |
|------------|---------------------|
| Alice      | HR                  |
| Bob        | Finance             |
| Charlie    | IT                  |
| Diana      | HR                  |
| Ethan      | Finance             |

---

### 7️⃣ **Subqueries**

#### Subquery in `WHERE` Clause
```sql
SELECT * FROM employees WHERE salary > (SELECT AVG(salary) FROM employees);
```
**Result:** Displays employees earning above the average salary.

---

### 8️⃣ **Views**

#### Create a View
```sql
CREATE VIEW high_earners AS
SELECT name, salary FROM employees WHERE salary > 70000;
```

#### Query the View
```sql
SELECT * FROM high_earners;
```
**Result:**
| **name**   | **salary** |
|------------|------------|
| Bob        | 75000.00   |
| Ethan      | 80000.00   |

---

### 9️⃣ **Transactions**

#### Transaction Example
```sql
START TRANSACTION;

UPDATE employees SET salary = 90000 WHERE name = 'Alice';
ROLLBACK;  -- Undo the change

UPDATE employees SET salary = 90000 WHERE name = 'Alice';
COMMIT;  -- Save the change
```

---

### 🔥 **Summary of Queries**

| **Query Type**        | **Example Query**                                                                 |
|-----------------------|-----------------------------------------------------------------------------------|
| **Select Data**       | `SELECT * FROM employees;`                                                       |
| **Insert Data**       | `INSERT INTO employees (name, age) VALUES ('John', 40);`                         |
| **Update Data**       | `UPDATE employees SET salary = 70000 WHERE name = 'Alice';`                      |
| **Delete Data**       | `DELETE FROM employees WHERE age > 50;`                                         |
| **Aggregate Functions**| `SELECT AVG(salary) FROM employees;`                                            |
| **Grouping**          | `SELECT department, COUNT(*) FROM employees GROUP BY department;`                |
| **Joining Tables**    | `SELECT employees.name, departments.name FROM employees INNER JOIN departments;` |
| **Subqueries**        | `SELECT * FROM employees WHERE salary > (SELECT AVG(salary) FROM employees);`     |
| **Transactions**      | `START TRANSACTION; ROLLBACK; COMMIT;`                                           |


****
****




























