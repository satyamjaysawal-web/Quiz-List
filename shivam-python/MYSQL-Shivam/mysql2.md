### 🔥 **Data Retrieval & Querying in SQL**

Data retrieval and querying in SQL is done primarily using the **`SELECT`** statement. It allows users to fetch, filter, sort, group, and aggregate data from one or more tables. Below is a comprehensive guide to SQL querying for data retrieval.

---

### 1️⃣ **Basic Retrieval**
#### Select All Columns
```sql
SELECT * FROM table_name;
```
- Retrieves all columns from the table.
```sql
SELECT * FROM employees;
```

#### Select Specific Columns
```sql
SELECT column1, column2 FROM table_name;
```
- Fetches only specific columns.
```sql
SELECT name, salary FROM employees;
```

---

### 2️⃣ **Filtering Data**
#### `WHERE` Clause
- Filters rows based on a condition.
```sql
SELECT * FROM employees WHERE department = 'HR';
```

#### Logical Operators
- Combine multiple conditions with `AND`, `OR`, and `NOT`.
```sql
SELECT * FROM employees WHERE age > 30 AND department = 'Finance';
```

#### Pattern Matching with `LIKE`
- Searches for patterns in string data.
```sql
SELECT * FROM employees WHERE name LIKE 'A%';  -- Names starting with 'A'
SELECT * FROM employees WHERE name LIKE '%n';  -- Names ending with 'n'
```

#### Range Filter with `BETWEEN`
- Filters rows within a specific range.
```sql
SELECT * FROM employees WHERE salary BETWEEN 60000 AND 80000;
```

#### Match Specific Values with `IN`
- Matches any value in a list.
```sql
SELECT * FROM employees WHERE department IN ('HR', 'Finance');
```

---

### 3️⃣ **Sorting Data**
#### `ORDER BY`
- Sorts data in ascending (`ASC`) or descending (`DESC`) order.
```sql
SELECT * FROM employees ORDER BY salary DESC;
```

---

### 4️⃣ **Limiting Results**
#### `LIMIT`
- Limits the number of rows returned.
```sql
SELECT * FROM employees ORDER BY salary DESC LIMIT 5;
```

#### Offset Results
- Skips a specified number of rows before returning the results.
```sql
SELECT * FROM employees ORDER BY salary DESC LIMIT 5 OFFSET 10;  -- Rows 11-15
```

---

### 5️⃣ **Aggregate Functions**
- Perform calculations on groups of rows and return a single result.

#### Count Rows
```sql
SELECT COUNT(*) AS total_employees FROM employees;
```

#### Calculate Total
```sql
SELECT SUM(salary) AS total_salary FROM employees;
```

#### Find Average
```sql
SELECT AVG(salary) AS average_salary FROM employees;
```

#### Find Minimum and Maximum
```sql
SELECT MIN(salary) AS min_salary, MAX(salary) AS max_salary FROM employees;
```

---

### 6️⃣ **Grouping Data**
#### `GROUP BY`
- Groups rows based on one or more columns.
```sql
SELECT department, COUNT(*) AS total_employees FROM employees GROUP BY department;
```

#### Filtering Groups with `HAVING`
- Filters aggregated data.
```sql
SELECT department, AVG(salary) AS avg_salary 
FROM employees 
GROUP BY department 
HAVING avg_salary > 60000;
```

---

### 7️⃣ **Joining Tables**
- Combines rows from multiple tables based on related columns.

#### Inner Join
- Retrieves rows that have matching values in both tables.
```sql
SELECT employees.name, departments.name AS department_name
FROM employees
INNER JOIN departments ON employees.department_id = departments.id;
```

#### Left Join
- Retrieves all rows from the left table, and matching rows from the right table.
```sql
SELECT employees.name, departments.name AS department_name
FROM employees
LEFT JOIN departments ON employees.department_id = departments.id;
```

---

### 8️⃣ **Subqueries**
- Query inside another query.

#### Subquery in `WHERE`
```sql
SELECT name, salary 
FROM employees 
WHERE salary > (SELECT AVG(salary) FROM employees);
```

#### Subquery in `SELECT`
```sql
SELECT name, 
       (SELECT department FROM departments WHERE departments.id = employees.department_id) AS department_name
FROM employees;
```

---

### 9️⃣ **Full-Text Search**
- Search for text patterns in large text columns using a full-text index.
```sql
CREATE FULLTEXT INDEX idx_description ON products(description);
SELECT * FROM products WHERE MATCH(description) AGAINST('laptop');
```

---

### 🔍 **Query Optimization Techniques**
1. **Use Indexes**:
   - Ensure indexed columns are used in `WHERE`, `JOIN`, or `ORDER BY` clauses.
   ```sql
   EXPLAIN SELECT * FROM employees WHERE name = 'Alice';
   ```

2. **Avoid `SELECT *`**:
   - Select only the required columns.
   ```sql
   SELECT name, salary FROM employees;
   ```

3. **Limit Results**:
   - Use `LIMIT` to fetch only necessary rows.

4. **Analyze Query Performance**:
   - Use `EXPLAIN` to understand how MySQL executes a query.
   ```sql
   EXPLAIN SELECT * FROM employees WHERE department = 'HR';
   ```

5. **Use Joins Instead of Subqueries**:
   - Joins are generally faster and more efficient than subqueries.

---

### 1️⃣0️⃣ **Advanced Querying**
#### Case Statement
- Add conditional logic to queries.
```sql
SELECT name, 
       CASE 
           WHEN salary > 70000 THEN 'High'
           WHEN salary BETWEEN 50000 AND 70000 THEN 'Medium'
           ELSE 'Low'
       END AS salary_range
FROM employees;
```

#### Window Functions
- Perform calculations across a set of rows related to the current row.
```sql
SELECT name, salary, 
       RANK() OVER (ORDER BY salary DESC) AS rank
FROM employees;
```

#### Common Table Expressions (CTEs)
- Define temporary result sets for use within a query.
```sql
WITH high_earners AS (
    SELECT name, salary FROM employees WHERE salary > 70000
)
SELECT * FROM high_earners;
```

---

### 🔥 **Summary**

| **Feature**           | **Command** or **Clause**                                                             |
|-----------------------|---------------------------------------------------------------------------------------|
| **Basic Query**       | `SELECT`, `WHERE`, `ORDER BY`, `LIMIT`                                               |
| **Filtering Data**    | `WHERE`, `BETWEEN`, `LIKE`, `IN`                                                     |
| **Sorting**           | `ORDER BY`                                                                           |
| **Aggregation**       | `COUNT`, `SUM`, `AVG`, `MIN`, `MAX`                                                  |
| **Grouping**          | `GROUP BY`, `HAVING`                                                                 |
| **Joins**             | `INNER JOIN`, `LEFT JOIN`                                                            |
| **Subqueries**        | `SELECT ... WHERE (SELECT ...)`, `SELECT ... IN (SELECT ...)`                        |
| **Text Search**       | `MATCH ... AGAINST`                                                                  |
| **Advanced Queries**  | `CASE`, `RANK()`, `WITH`                                                             |
| **Optimization**      | Use `EXPLAIN`, `LIMIT`, and indexes to optimize performance.                         |

****
****





















****

****


















****
****

