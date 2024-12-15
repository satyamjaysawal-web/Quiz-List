


### **Expanded SQL Clauses, Commands, and Examples**



---

| **Clause/Command** | **Purpose**                                           | **Example**                                                    |
|---------------------|-------------------------------------------------------|----------------------------------------------------------------|
| **`WHERE`**         | Filter rows before grouping or aggregation.           | `WHERE age > 30;`                                             |
| **`HAVING`**        | Filter rows after grouping or aggregation.            | `HAVING total_salary > 100000;`                               |
| **`GROUP BY`**      | Group rows with the same values.                      | `GROUP BY department;`                                        |
| **`ORDER BY`**      | Sort rows in ascending or descending order.           | `ORDER BY salary DESC;`                                       |
| **`LIMIT`**         | Restrict the number of rows returned.                 | `LIMIT 5;`                                                   |
| **`OFFSET`**        | Skip a specific number of rows before returning results. | `LIMIT 5 OFFSET 10;` (Rows 11–15)                            |
| **`JOIN`**          | Combine rows from multiple tables.                    | `JOIN departments ON employees.department_id = departments.id;` |
| **`INNER JOIN`**    | Combine rows with matching values in both tables.     | `SELECT * FROM employees INNER JOIN departments ON employees.department_id = departments.id;` |
| **`LEFT JOIN`**     | Combine rows and keep unmatched rows from the left table. | `LEFT JOIN departments ON employees.department_id = departments.id;` |
| **`RIGHT JOIN`**    | Combine rows and keep unmatched rows from the right table. | `RIGHT JOIN departments ON employees.department_id = departments.id;` |
| **`FULL OUTER JOIN`** | Combine rows, keeping unmatched rows from both tables. | `FULL OUTER JOIN departments ON employees.department_id = departments.id;` |
| **`CROSS JOIN`**    | Combine all rows from two tables (Cartesian Product). | `CROSS JOIN departments;`                                     |
| **`SELF JOIN`**     | Join a table with itself.                             | `SELECT e1.name, e2.name FROM employees e1, employees e2 WHERE e1.manager_id = e2.id;` |
| **`UNION`**         | Combine results of two queries (no duplicates).       | `SELECT name FROM employees UNION SELECT name FROM managers;` |
| **`UNION ALL`**     | Combine results of two queries (allows duplicates).   | `SELECT name FROM employees UNION ALL SELECT name FROM managers;` |
| **`SELECT`**        | Retrieve data from a table.                           | `SELECT name, salary FROM employees;`                         |
| **`INSERT`**        | Add new rows to a table.                              | `INSERT INTO employees (name, salary) VALUES ('Alice', 60000);` |
| **`UPDATE`**        | Modify existing rows in a table.                      | `UPDATE employees SET salary = 70000 WHERE id = 1;`           |
| **`DELETE`**        | Remove rows from a table.                             | `DELETE FROM employees WHERE age > 60;`                       |
| **`CREATE`**        | Create a new database object.                         | `CREATE TABLE employees (id INT, name VARCHAR(100));`         |
| **`ALTER`**         | Modify the structure of a table.                      | `ALTER TABLE employees ADD COLUMN age INT;`                   |
| **`DROP`**          | Delete a table or database object.                    | `DROP TABLE employees;`                                       |
| **`TRUNCATE`**      | Delete all rows from a table (structure remains).     | `TRUNCATE TABLE employees;`                                   |
| **`EXPLAIN`**       | Show how a query will be executed.                    | `EXPLAIN SELECT * FROM employees WHERE age > 30;`             |
| **`CASE`**          | Add conditional logic in queries.                    | `SELECT name, CASE WHEN salary > 70000 THEN 'High' ELSE 'Low' END AS salary_range FROM employees;` |
| **`LIKE`**          | Perform pattern matching.                            | `SELECT * FROM employees WHERE name LIKE 'A%';`               |
| **`IN`**            | Match any value in a list.                           | `SELECT * FROM employees WHERE department IN ('HR', 'IT');`   |
| **`BETWEEN`**       | Filter values within a range.                        | `SELECT * FROM employees WHERE salary BETWEEN 50000 AND 80000;` |
| **`DISTINCT`**      | Select unique values from a column.                  | `SELECT DISTINCT department FROM employees;`                 |
| **`SUBQUERY`**      | Use a query within another query.                    | `SELECT name FROM employees WHERE salary > (SELECT AVG(salary) FROM employees);` |
| **`VIEW`**          | Create a virtual table from a query.                 | `CREATE VIEW high_earners AS SELECT name, salary FROM employees WHERE salary > 80000;` |
| **`INDEX`**         | Create an index to improve query performance.        | `CREATE INDEX idx_salary ON employees(salary);`              |
| **`GRANT`**         | Provide access privileges to a user.                 | `GRANT SELECT ON employees TO user1;`                        |
| **`REVOKE`**        | Remove access privileges from a user.                | `REVOKE SELECT ON employees FROM user1;`                     |
| **`START TRANSACTION`** | Begin a transaction for multiple queries.           | `START TRANSACTION;`                                         |
| **`COMMIT`**        | Save changes made during a transaction.              | `COMMIT;`                                                    |
| **`ROLLBACK`**      | Undo changes made during a transaction.              | `ROLLBACK;`                                                  |
| **`SAVEPOINT`**     | Set a point within a transaction for partial rollbacks. | `SAVEPOINT sp1;`                                            |
| **`SET`**           | Set configuration variables for the session.         | `SET autocommit = 0;`                                        |
| **`SHOW`**          | Display information about databases, tables, or configurations. | `SHOW DATABASES;`, `SHOW TABLES;`                            |
| **`DESCRIBE`**      | Display the structure of a table.                    | `DESCRIBE employees;`                                        |
| **`FULLTEXT`**      | Perform full-text searches on indexed columns.       | `SELECT * FROM products WHERE MATCH(description) AGAINST('laptop');` |

---

****

### **`WHERE` vs. `HAVING` with Dry Run**

A **dry run** explains how a query is processed step by step, showing the intermediate results after applying **`WHERE`** and **`HAVING`** clauses. Let’s explore these clauses with detailed dry-run examples using the **`employees`** table.

---

### **Sample Table: `employees`**

| **id** | **name**   | **department** | **age** | **salary** |
|--------|------------|----------------|---------|------------|
| 1      | Alice      | HR             | 30      | 60000      |
| 2      | Bob        | Finance        | 45      | 75000      |
| 3      | Charlie    | IT             | 25      | 50000      |
| 4      | Diana      | HR             | 35      | 65000      |
| 5      | Ethan      | Finance        | 50      | 80000      |

---

### **Scenario 1: Using `WHERE`**

#### Query:
Find all employees in the `Finance` department with a salary greater than 70,000.
```sql
SELECT name, department, salary
FROM employees
WHERE department = 'Finance' AND salary > 70000;
```

#### Dry Run:
1. **Step 1**: Start with the full `employees` table.
   ```
   | id | name     | department | age | salary  |
   |----|----------|------------|-----|---------|
   | 1  | Alice    | HR         | 30  | 60000   |
   | 2  | Bob      | Finance    | 45  | 75000   |
   | 3  | Charlie  | IT         | 25  | 50000   |
   | 4  | Diana    | HR         | 35  | 65000   |
   | 5  | Ethan    | Finance    | 50  | 80000   |
   ```

2. **Step 2**: Apply the condition `department = 'Finance'`.
   ```
   | id | name     | department | age | salary  |
   |----|----------|------------|-----|---------|
   | 2  | Bob      | Finance    | 45  | 75000   |
   | 5  | Ethan    | Finance    | 50  | 80000   |
   ```

3. **Step 3**: Apply the condition `salary > 70000`.
   ```
   | id | name     | department | age | salary  |
   |----|----------|------------|-----|---------|
   | 2  | Bob      | Finance    | 45  | 75000   |
   | 5  | Ethan    | Finance    | 50  | 80000   |
   ```

4. **Result**: Only employees who satisfy both conditions are included.
   ```
   | name     | department | salary  |
   |----------|------------|---------|
   | Bob      | Finance    | 75000   |
   | Ethan    | Finance    | 80000   |
   ```

---

### **Scenario 2: Using `HAVING`**

#### Query:
Find departments where the total salary exceeds 130,000.
```sql
SELECT department, SUM(salary) AS total_salary
FROM employees
GROUP BY department
HAVING SUM(salary) > 130000;
```

#### Dry Run:
1. **Step 1**: Start with the full `employees` table.
   ```
   | id | name     | department | age | salary  |
   |----|----------|------------|-----|---------|
   | 1  | Alice    | HR         | 30  | 60000   |
   | 2  | Bob      | Finance    | 45  | 75000   |
   | 3  | Charlie  | IT         | 25  | 50000   |
   | 4  | Diana    | HR         | 35  | 65000   |
   | 5  | Ethan    | Finance    | 50  | 80000   |
   ```

2. **Step 2**: Group rows by `department`.
   ```
   Groups:
   - HR:    Alice, Diana
   - Finance: Bob, Ethan
   - IT:    Charlie
   ```

3. **Step 3**: Calculate the aggregate `SUM(salary)` for each group.
   ```
   | department | total_salary |
   |------------|--------------|
   | HR         | 125000       |
   | Finance    | 155000       |
   | IT         | 50000        |
   ```

4. **Step 4**: Apply the `HAVING` condition `SUM(salary) > 130000`.
   ```
   | department | total_salary |
   |------------|--------------|
   | Finance    | 155000       |
   ```

5. **Result**: Only the departments meeting the condition are included.
   ```
   | department | total_salary |
   |------------|--------------|
   | Finance    | 155000       |
   ```

---

### **Scenario 3: Using Both `WHERE` and `HAVING`**

#### Query:
Find departments where employees older than 30 have a total salary greater than 130,000.
```sql
SELECT department, SUM(salary) AS total_salary
FROM employees
WHERE age > 30
GROUP BY department
HAVING SUM(salary) > 130000;
```

#### Dry Run:
1. **Step 1**: Start with the full `employees` table.
   ```
   | id | name     | department | age | salary  |
   |----|----------|------------|-----|---------|
   | 1  | Alice    | HR         | 30  | 60000   |
   | 2  | Bob      | Finance    | 45  | 75000   |
   | 3  | Charlie  | IT         | 25  | 50000   |
   | 4  | Diana    | HR         | 35  | 65000   |
   | 5  | Ethan    | Finance    | 50  | 80000   |
   ```

2. **Step 2**: Apply the `WHERE` condition `age > 30` (filters rows before grouping).
   ```
   | id | name     | department | age | salary  |
   |----|----------|------------|-----|---------|
   | 2  | Bob      | Finance    | 45  | 75000   |
   | 4  | Diana    | HR         | 35  | 65000   |
   | 5  | Ethan    | Finance    | 50  | 80000   |
   ```

3. **Step 3**: Group the filtered rows by `department`.
   ```
   Groups:
   - HR: Diana
   - Finance: Bob, Ethan
   ```

4. **Step 4**: Calculate the aggregate `SUM(salary)` for each group.
   ```
   | department | total_salary |
   |------------|--------------|
   | HR         | 65000        |
   | Finance    | 155000       |
   ```

5. **Step 5**: Apply the `HAVING` condition `SUM(salary) > 130000` (filters aggregated results).
   ```
   | department | total_salary |
   |------------|--------------|
   | Finance    | 155000       |
   ```

6. **Result**:
   ```
   | department | total_salary |
   |------------|--------------|
   | Finance    | 155000       |
   ```

---

### **Key Takeaways**

1. **`WHERE` Filters Rows Before Aggregation**:
   - Filters raw data rows before grouping or aggregate calculations.
   - Works on individual column values.

2. **`HAVING` Filters Groups After Aggregation**:
   - Filters groups or results of aggregate calculations.
   - Works on aggregate functions like `SUM`, `AVG`, `COUNT`.

---

### **Comparison Summary**

| **Aspect**         | **`WHERE`**                                    | **`HAVING`**                                 |
|--------------------|-----------------------------------------------|---------------------------------------------|
| **Filters Applied** | Before grouping or aggregation.               | After grouping or aggregation.              |
| **Works With**      | Column values (non-aggregated data).           | Aggregate functions (`SUM`, `AVG`, etc.).   |
| **Execution Stage** | Early in query execution.                     | Later in query execution.                   |
| **Example**         | `WHERE age > 30`                              | `HAVING SUM(salary) > 130000`               |





****

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
### 🔥 **Indexing in MySQL**

An **index** in MySQL is a data structure used to optimize the performance of queries by allowing faster retrieval of rows from a table. Indexes reduce the amount of data that needs to be scanned to locate the required rows, making queries significantly faster.

---

### 🔍 **Types of Indexes in MySQL**

1. **Primary Index**
   - Automatically created for the **primary key** column(s) of a table.
   - Ensures **uniqueness** of the key and optimizes lookups.
   - Only one primary index per table.

   ```sql
   CREATE TABLE employees (
       id INT PRIMARY KEY,
       name VARCHAR(100),
       age INT
   );
   ```

2. **Unique Index**
   - Ensures all values in the indexed column are unique.
   - A table can have multiple unique indexes.

   ```sql
   CREATE UNIQUE INDEX idx_email ON employees (email);
   ```

3. **Simple Index**
   - A basic index that does not enforce uniqueness.
   - Often used to optimize searches on specific columns.

   ```sql
   CREATE INDEX idx_name ON employees (name);
   ```

4. **Composite Index**
   - An index on multiple columns.
   - Optimizes queries that use all or part of the indexed columns in the `WHERE` clause.

   ```sql
   CREATE INDEX idx_name_age ON employees (name, age);
   ```

5. **Full-Text Index**
   - Used for full-text search capabilities.
   - Works only on **CHAR**, **VARCHAR**, or **TEXT** columns.

   ```sql
   CREATE FULLTEXT INDEX idx_description ON products (description);
   ```

6. **Spatial Index**
   - Used for geospatial data types (e.g., POINT, LINESTRING, POLYGON).
   - Requires a table to use the **InnoDB** or **MyISAM** engine.

   ```sql
   CREATE SPATIAL INDEX idx_location ON locations (coordinates);
   ```

---

### 📋 **How to Create Indexes in MySQL**

#### 1️⃣ Create Index at Table Creation
You can define indexes while creating a table.

```sql
CREATE TABLE employees (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100) UNIQUE,
    age INT,
    department VARCHAR(50),
    INDEX idx_department (department)
);
```

#### 2️⃣ Create Index on Existing Table
Indexes can also be added to existing tables.

```sql
CREATE INDEX idx_salary ON employees (salary);
```

#### 3️⃣ Using `ALTER TABLE` to Add an Index
```sql
ALTER TABLE employees ADD INDEX idx_joining_date (joining_date);
```

#### 4️⃣ Create Composite Index
```sql
CREATE INDEX idx_name_salary ON employees (name, salary);
```

#### 5️⃣ Create Full-Text Index
```sql
CREATE FULLTEXT INDEX idx_desc ON products (description);
```

---

### 🗑 **How to Remove Indexes in MySQL**

1. **Drop Index**
   - Use the `DROP INDEX` statement to remove an index.

   ```sql
   DROP INDEX idx_salary ON employees;
   ```

2. **Using `ALTER TABLE`**
   ```sql
   ALTER TABLE employees DROP INDEX idx_joining_date;
   ```

---

### 🛠 **How Indexing Works**

#### Without Index:
- The database scans all rows (a **full table scan**) to find matching rows for the query.

#### With Index:
- The database uses the index to directly locate the rows, avoiding a full scan.

---

### 🔑 **Key Indexing Concepts**

1. **B-Tree Structure**
   - Most MySQL indexes use the **B-Tree** structure.
   - Optimized for range queries and equality searches.
   - Suitable for `PRIMARY KEY`, `UNIQUE`, `INDEX`, and composite indexes.

2. **Clustered Index**
   - The table's primary key is stored with the data in the same structure (used in **InnoDB** tables).

3. **Non-Clustered Index**
   - Separate from the data and contains pointers to the table rows (used in **MyISAM** tables).

4. **Cardinality**
   - Refers to the number of unique values in an indexed column.
   - High cardinality (e.g., IDs) is more efficient for indexing than low cardinality (e.g., gender).

---

### 📈 **Best Practices for Indexing**

1. **Index Frequently Queried Columns**
   - Add indexes to columns used in the `WHERE`, `JOIN`, `GROUP BY`, and `ORDER BY` clauses.

2. **Use Composite Indexes Carefully**
   - Place the most selective column (the one with the most unique values) first.
   ```sql
   CREATE INDEX idx_name_age ON employees (name, age);
   ```

3. **Avoid Indexing Low Cardinality Columns**
   - Columns like `gender` or `is_active` with only a few unique values are not ideal for indexing.

4. **Limit the Number of Indexes**
   - Too many indexes increase write operation costs (e.g., `INSERT`, `UPDATE`, `DELETE`) because all indexes must be updated.

5. **Use Full-Text Index for Search**
   - Use a full-text index for text-heavy fields like descriptions, comments, or logs.

6. **Monitor Index Usage**
   - Use the `EXPLAIN` statement to check whether a query uses an index.
   ```sql
   EXPLAIN SELECT * FROM employees WHERE name = 'Alice';
   ```

---

### ⚡ **Advantages of Indexing**

1. **Faster Query Performance**
   - Queries retrieve data faster by reducing the number of rows scanned.

2. **Efficient Sorting**
   - Indexes can improve the performance of `ORDER BY` clauses.

3. **Enhanced Join Performance**
   - Joining large tables becomes more efficient when indexes are present on join keys.

4. **Primary Key Enforcement**
   - Indexes ensure that primary keys are unique and non-null.

---

### ⚠️ **Disadvantages of Indexing**

1. **Increased Storage**
   - Indexes consume additional storage.

2. **Slower Writes**
   - Insert, update, and delete operations take longer because indexes need to be updated.

3. **Complex Maintenance**
   - Frequent changes to data structures may require re-creating indexes.

---

### 🔍 **Analyze Indexes**

#### Check Existing Indexes
```sql
SHOW INDEX FROM employees;
```

#### Analyze Query Performance
```sql
EXPLAIN SELECT * FROM employees WHERE name = 'Alice';
```

**Sample Output of `EXPLAIN`:**
| **id** | **select_type** | **table** | **type** | **possible_keys** | **key**   | **rows** | **Extra**          |
|--------|-----------------|-----------|----------|-------------------|-----------|---------|--------------------|
| 1      | SIMPLE          | employees | ref      | idx_name          | idx_name  | 1       | Using index        |

---

### Example Workflow: Adding and Using Indexes

#### 1️⃣ Create a Table Without Index
```sql
CREATE TABLE employees (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    age INT,
    department VARCHAR(50),
    salary DECIMAL(10, 2)
);
```

#### 2️⃣ Insert Data
```sql
INSERT INTO employees (name, age, department, salary)
VALUES 
('Alice', 30, 'HR', 60000),
('Bob', 45, 'Finance', 75000),
('Charlie', 25, 'IT', 50000),
('Diana', 35, 'HR', 65000),
('Ethan', 50, 'Finance', 80000);
```

#### 3️⃣ Query Without Index
```sql
SELECT * FROM employees WHERE department = 'HR';
-- Full table scan occurs (slow for large tables)
```

#### 4️⃣ Add an Index
```sql
CREATE INDEX idx_department ON employees (department);
```

#### 5️⃣ Query With Index
```sql
SELECT * FROM employees WHERE department = 'HR';
-- Query now uses the index (faster)
```

---
****

****


### 🔥 **Data Integrity and Constraints in SQL**

**Data Integrity** refers to the accuracy, consistency, and reliability of data stored in a database. **Constraints** are rules enforced at the database level to maintain data integrity. Together, they ensure that the data remains valid and usable, preventing invalid, inconsistent, or corrupted data.

---

### 🔑 **Types of Data Integrity**

1. **Entity Integrity**  
   - Ensures that every table has a unique identifier (primary key).
   - No two rows can have the same value for the primary key, and primary key values cannot be `NULL`.

2. **Referential Integrity**  
   - Ensures consistency between related tables through **foreign keys**.
   - Prevents actions that would leave orphaned rows or break relationships.

3. **Domain Integrity**  
   - Ensures data stored in a column adheres to predefined rules, such as data type, format, and range.
   - Enforced through constraints like `CHECK`, `NOT NULL`, and data types.

4. **User-Defined Integrity**  
   - Custom rules defined to meet specific business requirements.
   - Implemented using triggers, stored procedures, or application logic.

---

### 🔍 **Types of Constraints**

Constraints are used to define rules for the data in a table. They can be applied at the **column level** (for a single column) or the **table level** (for multiple columns).

| **Constraint**      | **Description**                                                   |
|---------------------|-------------------------------------------------------------------|
| **NOT NULL**        | Ensures a column cannot contain `NULL` values.                   |
| **UNIQUE**          | Ensures all values in a column are unique.                       |
| **PRIMARY KEY**     | Combines `NOT NULL` and `UNIQUE` to uniquely identify rows.      |
| **FOREIGN KEY**     | Establishes relationships between tables.                        |
| **CHECK**           | Ensures values in a column satisfy a specific condition.         |
| **DEFAULT**         | Assigns a default value if no value is provided for a column.    |

---

### 📋 **Detailed Explanation of Constraints**

#### 1️⃣ **NOT NULL**
- Prevents a column from having `NULL` values.
- Used to ensure mandatory fields.

**Syntax:**
```sql
CREATE TABLE employees (
    id INT NOT NULL,
    name VARCHAR(100) NOT NULL,
    age INT
);
```

**Example:**
```sql
INSERT INTO employees (id, name) VALUES (1, 'Alice'); -- Valid
INSERT INTO employees (id) VALUES (2); -- ❌ Error: "name" cannot be NULL
```

---

#### 2️⃣ **UNIQUE**
- Ensures all values in a column (or combination of columns) are unique.

**Syntax:**
```sql
CREATE TABLE employees (
    email VARCHAR(100) UNIQUE
);
```

**Example:**
```sql
INSERT INTO employees (email) VALUES ('alice@example.com'); -- Valid
INSERT INTO employees (email) VALUES ('alice@example.com'); -- ❌ Error: Duplicate entry
```

---

#### 3️⃣ **PRIMARY KEY**
- Combines `NOT NULL` and `UNIQUE` to uniquely identify rows in a table.
- A table can have only one primary key.

**Syntax:**
```sql
CREATE TABLE employees (
    id INT PRIMARY KEY,
    name VARCHAR(100)
);
```

**Example:**
```sql
INSERT INTO employees (id, name) VALUES (1, 'Alice'); -- Valid
INSERT INTO employees (id, name) VALUES (1, 'Bob'); -- ❌ Error: Duplicate primary key
```

---

#### 4️⃣ **FOREIGN KEY**
- Links two tables by creating a relationship between a column in one table and the primary key in another table.
- Ensures **referential integrity**.

**Syntax:**
```sql
CREATE TABLE departments (
    id INT PRIMARY KEY,
    name VARCHAR(100)
);

CREATE TABLE employees (
    id INT PRIMARY KEY,
    department_id INT,
    FOREIGN KEY (department_id) REFERENCES departments (id)
);
```

**Example:**
```sql
INSERT INTO departments (id, name) VALUES (1, 'HR'); -- Valid
INSERT INTO employees (id, department_id) VALUES (1, 1); -- Valid
INSERT INTO employees (id, department_id) VALUES (2, 99); -- ❌ Error: "department_id" 99 does not exist in "departments"
```

---

#### 5️⃣ **CHECK**
- Ensures values in a column meet a specific condition.

**Syntax:**
```sql
CREATE TABLE employees (
    id INT PRIMARY KEY,
    age INT CHECK (age >= 18 AND age <= 60)
);
```

**Example:**
```sql
INSERT INTO employees (id, age) VALUES (1, 25); -- Valid
INSERT INTO employees (id, age) VALUES (2, 17); -- ❌ Error: "age" must be between 18 and 60
```

---

#### 6️⃣ **DEFAULT**
- Assigns a default value to a column if no value is provided during insertion.

**Syntax:**
```sql
CREATE TABLE employees (
    id INT PRIMARY KEY,
    name VARCHAR(100),
    status VARCHAR(50) DEFAULT 'Active'
);
```

**Example:**
```sql
INSERT INTO employees (id, name) VALUES (1, 'Alice'); -- "status" will be 'Active'
```

---

### 📈 **Advantages of Constraints**

1. **Data Accuracy**
   - Prevents invalid or inconsistent data from being inserted into tables.

2. **Simplifies Validation**
   - Eliminates the need for repetitive validation logic in application code.

3. **Ensures Relationships**
   - Maintains referential integrity between related tables.

4. **Improves Query Performance**
   - Constraints like `PRIMARY KEY` and `UNIQUE` often create indexes, improving query speed.

---

### ⚠️ **Common Mistakes and Best Practices**

1. **Overusing Constraints**
   - Adding too many constraints can reduce flexibility in data manipulation. Use constraints judiciously.

2. **Testing Foreign Key Relationships**
   - Ensure referenced data exists in parent tables before inserting data in child tables.

3. **Avoiding Low-Cardinality Indexing**
   - Avoid creating unique constraints or indexes on columns with few distinct values, like `gender`.

4. **Use Default Values**
   - Always define default values for optional fields to prevent `NULL` unless explicitly required.

---

### 🛠 **Examples: Adding, Dropping, and Altering Constraints**

#### Add a Constraint to an Existing Table
```sql
ALTER TABLE employees ADD CONSTRAINT chk_salary CHECK (salary > 0);
```

#### Drop a Constraint
```sql
ALTER TABLE employees DROP CONSTRAINT chk_salary; -- For systems that support named constraints
```

#### Modify a Column with a Constraint
```sql
ALTER TABLE employees MODIFY COLUMN age INT NOT NULL;
```

---

### 🔥 **Summary of Data Integrity and Constraints**

| **Constraint**       | **Purpose**                                                        |
|-----------------------|--------------------------------------------------------------------|
| **NOT NULL**          | Prevents `NULL` values in a column.                               |
| **UNIQUE**            | Ensures all values in a column are unique.                        |
| **PRIMARY KEY**       | Uniquely identifies rows and ensures `NOT NULL`.                  |
| **FOREIGN KEY**       | Maintains referential integrity between tables.                   |
| **CHECK**             | Validates values against a condition.                             |
| **DEFAULT**           | Assigns default values when no value is provided.                |






























****
****


****
****



























