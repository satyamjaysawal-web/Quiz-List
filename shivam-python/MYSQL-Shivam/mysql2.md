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

### 🔥 **Normalization and Database Design**

**Normalization** is a systematic approach in database design to organize data efficiently and minimize redundancy. It involves dividing a database into tables and defining relationships to ensure data consistency and integrity. Proper database design using normalization improves performance and simplifies maintenance.

---

### **Key Objectives of Normalization**
1. **Eliminate Redundancy**: Avoid storing duplicate data.
2. **Ensure Data Integrity**: Maintain consistency across tables.
3. **Optimize Storage**: Save space by avoiding unnecessary data duplication.
4. **Facilitate Maintenance**: Make the database structure more understandable and easier to modify.

---

### **Normalization Forms**
Normalization is divided into several "normal forms" (NF), each with specific requirements.

---

#### 1️⃣ **First Normal Form (1NF)**

**Requirements**:
- The table should have a **primary key**.
- Each column should contain **atomic values** (indivisible data).
- No repeating groups or arrays.

**Example (Unnormalized Table)**:
| **ID** | **Name**   | **Subjects**         |
|--------|------------|----------------------|
| 1      | Alice      | Math, Physics        |
| 2      | Bob        | Chemistry, Biology   |

**Normalized to 1NF**:
| **ID** | **Name**   | **Subject**  |
|--------|------------|--------------|
| 1      | Alice      | Math         |
| 1      | Alice      | Physics      |
| 2      | Bob        | Chemistry    |
| 2      | Bob        | Biology      |

---

#### 2️⃣ **Second Normal Form (2NF)**

**Requirements**:
- Must meet **1NF** requirements.
- All **non-key attributes** must depend on the **whole primary key** (not part of it).
- Eliminate **partial dependency**.

**Example (1NF)**:
| **StudentID** | **CourseID** | **StudentName** | **CourseName** |
|---------------|--------------|-----------------|----------------|
| 1             | 101          | Alice           | Math           |
| 2             | 102          | Bob             | Physics        |

- `StudentName` depends only on `StudentID`.
- `CourseName` depends only on `CourseID`.

**Normalized to 2NF**:
**Student Table**:
| **StudentID** | **StudentName** |
|---------------|-----------------|
| 1             | Alice           |
| 2             | Bob             |

**Course Table**:
| **CourseID** | **CourseName** |
|--------------|----------------|
| 101          | Math           |
| 102          | Physics        |

**Enrollment Table**:
| **StudentID** | **CourseID** |
|---------------|--------------|
| 1             | 101          |
| 2             | 102          |

---

#### 3️⃣ **Third Normal Form (3NF)**

**Requirements**:
- Must meet **2NF** requirements.
- All **non-key attributes** must depend **only on the primary key**.
- Eliminate **transitive dependency**.

**Example (2NF)**:
| **EmployeeID** | **DepartmentID** | **DepartmentName** |
|----------------|-------------------|--------------------|
| 1              | 101               | HR                 |
| 2              | 102               | IT                 |

- `DepartmentName` depends on `DepartmentID`, not directly on `EmployeeID`.

**Normalized to 3NF**:
**Employee Table**:
| **EmployeeID** | **DepartmentID** |
|----------------|-------------------|
| 1              | 101               |
| 2              | 102               |

**Department Table**:
| **DepartmentID** | **DepartmentName** |
|------------------|---------------------|
| 101              | HR                  |
| 102              | IT                  |

---

#### 4️⃣ **Boyce-Codd Normal Form (BCNF)**

**Requirements**:
- A stricter version of **3NF**.
- Every determinant (column or set of columns that uniquely identifies another column) must be a **candidate key**.

**Example (3NF)**:
| **CourseID** | **InstructorID** | **InstructorName** |
|--------------|-------------------|--------------------|
| 101          | 1                 | Alice              |
| 102          | 1                 | Alice              |

- `InstructorName` depends on `InstructorID` but not on the primary key (`CourseID`).

**Normalized to BCNF**:
**Course Table**:
| **CourseID** | **InstructorID** |
|--------------|-------------------|
| 101          | 1                 |
| 102          | 1                 |

**Instructor Table**:
| **InstructorID** | **InstructorName** |
|------------------|---------------------|
| 1                | Alice              |

---

#### 5️⃣ **Fourth Normal Form (4NF)**

**Requirements**:
- Must meet **BCNF** requirements.
- No **multivalued dependencies**.

**Example (BCNF)**:
| **StudentID** | **Hobby**  | **Skill**  |
|---------------|------------|------------|
| 1             | Reading    | Python     |
| 1             | Cycling    | Python     |
| 1             | Reading    | SQL        |

**Normalized to 4NF**:
**Student-Hobby Table**:
| **StudentID** | **Hobby**  |
|---------------|------------|
| 1             | Reading    |
| 1             | Cycling    |

**Student-Skill Table**:
| **StudentID** | **Skill**  |
|---------------|------------|
| 1             | Python     |
| 1             | SQL        |

---

### **Steps for Database Design**

1. **Requirement Analysis**:
   - Understand the data requirements of the system.
   - Identify entities (e.g., students, courses) and relationships (e.g., enrollment).

2. **Conceptual Design**:
   - Use an **ER (Entity-Relationship)** diagram to represent the data model.
   - Identify entities, attributes, and relationships.
   - Define cardinality (e.g., one-to-one, one-to-many).

   Example:
   - Entity: `Student`
     - Attributes: `StudentID`, `Name`, `Age`

3. **Logical Design**:
   - Convert the ER diagram into a relational schema.
   - Apply normalization to eliminate redundancy and ensure integrity.

4. **Physical Design**:
   - Define storage details such as indexes, constraints, and data types.
   - Optimize the schema for query performance.

5. **Implementation**:
   - Use SQL to create tables, relationships, and constraints.

---

### **Best Practices for Database Design**

1. **Follow Normalization Rules**:
   - Ensure the schema meets at least **3NF** to minimize redundancy.
   - Consider denormalization only for performance-critical scenarios.

2. **Define Primary and Foreign Keys**:
   - Ensure every table has a **primary key**.
   - Use **foreign keys** to enforce relationships.

3. **Use Appropriate Data Types**:
   - Select data types that fit the data being stored (e.g., `VARCHAR(100)` for names, `DATE` for dates).

4. **Add Indexes**:
   - Create indexes on frequently queried columns to improve performance.
   - Avoid indexing low-cardinality columns.

5. **Avoid Over-Normalization**:
   - While normalization reduces redundancy, excessive normalization can lead to complex joins and impact performance.

6. **Plan for Scalability**:
   - Design for growth, considering the potential increase in data volume.

---

### **Example: Normalized Database Design**

#### **ER Diagram Example**
Entities:
- `Student` (Attributes: `StudentID`, `Name`, `Age`)
- `Course` (Attributes: `CourseID`, `CourseName`)
- `Enrollment` (Attributes: `StudentID`, `CourseID`, `EnrollmentDate`)

#### **Relational Schema**
1. **Student Table**:
   ```sql
   CREATE TABLE Student (
       StudentID INT PRIMARY KEY,
       Name VARCHAR(100),
       Age INT
   );
   ```

2. **Course Table**:
   ```sql
   CREATE TABLE Course (
       CourseID INT PRIMARY KEY,
       CourseName VARCHAR(100)
   );
   ```

3. **Enrollment Table**:
   ```sql
   CREATE TABLE Enrollment (
       StudentID INT,
       CourseID INT,
       EnrollmentDate DATE,
       PRIMARY KEY (StudentID, CourseID),
       FOREIGN KEY (StudentID) REFERENCES Student(StudentID),
       FOREIGN KEY (CourseID) REFERENCES Course(CourseID)
   );
   ```

---

### **Advantages of Normalization**
1. **Data Integrity**:
   - Ensures consistent and accurate data.

2. **Reduced Redundancy**:
   - Avoids duplication, saving storage space.

3. **Improved Query Performance**:
   - Queries become faster with optimized relationships and indexes.

4. **Flexibility**:
   - Easier to modify and update the schema without affecting data integrity.

---

### **Disadvantages of Normalization**
1. **Complex Joins**:
   - Normalization often leads to many small tables, resulting in complex joins for queries.

2. **Performance Overhead**:
   - Over-normalization can slow down read-heavy queries.

3. **Higher Design Effort**:
   - Initial design requires thorough understanding and planning.

---

### 🔥 **Summary**

| **Normalization Form** | **Objective**                       | **Key Feature**                                         |
|-------------------------|-------------------------------------|--------------------------------------------------------|
| **1NF**                | Eliminate repeating groups          | Atomic columns, unique rows                           |
| **2NF**                | Eliminate partial dependencies      | Full functional dependency                            |
| **3NF**                | Eliminate transitive dependencies   | Non-key attributes depend only on primary key         |
| **BCNF**               | Stricter version of 3NF             | Determinants must be candidate keys                  |
| **4NF**                | Eliminate multivalued dependencies  | Separate independent multivalued attributes           |


****
****

### 🔥 **Views in MySQL**

A **view** in MySQL is a virtual table based on the result set of a SQL query. It does not store data physically but provides a dynamic, logical representation of data from one or more tables.

---

### **Key Features of Views**
1. **Virtual Table**: Views do not store data themselves; they fetch data dynamically when queried.
2. **Simplifies Complex Queries**: Encapsulates complex SQL queries into reusable objects.
3. **Data Security**: Restricts access to specific columns or rows for certain users.
4. **Up-to-Date**: Reflects the latest data from the base tables.
5. **Read-Only or Updatable**: Views can be read-only or updatable (with certain restrictions).

---

### **Syntax for Creating a View**

```sql
CREATE VIEW view_name AS
SELECT columns
FROM table_name
WHERE condition;
```

---

### **Examples**

#### 1️⃣ Simple View
Create a view to show employees from the HR department.
```sql
CREATE VIEW hr_employees AS
SELECT id, name, salary
FROM employees
WHERE department = 'HR';
```

Query the view:
```sql
SELECT * FROM hr_employees;
```

#### 2️⃣ View with Joins
Create a view to display employees along with their department names from a `departments` table.
```sql
CREATE VIEW employee_details AS
SELECT e.id, e.name, e.salary, d.department_name
FROM employees e
JOIN departments d ON e.department_id = d.id;
```

Query the view:
```sql
SELECT * FROM employee_details;
```

---

### **Querying a View**

You can use a view just like a table:
```sql
SELECT * FROM view_name WHERE condition;
```

**Example**:
```sql
SELECT name, salary FROM hr_employees WHERE salary > 60000;
```

---

### **Modifying a View**

#### 1️⃣ Update View
```sql
CREATE OR REPLACE VIEW view_name AS
SELECT new_columns
FROM table_name
WHERE new_condition;
```

**Example**:
```sql
CREATE OR REPLACE VIEW hr_employees AS
SELECT id, name
FROM employees
WHERE department = 'HR' AND salary > 50000;
```

#### 2️⃣ Add Columns to View
Modify the view to include an additional column:
```sql
CREATE OR REPLACE VIEW hr_employees AS
SELECT id, name, salary, joining_date
FROM employees
WHERE department = 'HR';
```

---

### **Deleting a View**

Use the `DROP VIEW` statement to delete a view:
```sql
DROP VIEW view_name;
```

**Example**:
```sql
DROP VIEW hr_employees;
```

---

### **Updatable vs. Read-Only Views**

#### Updatable Views
- Allows `INSERT`, `UPDATE`, and `DELETE` operations on the view.
- Must adhere to certain rules:
  - View must reference only one table.
  - No aggregate functions, `DISTINCT`, or `GROUP BY` clauses in the view.

**Example**:
```sql
CREATE VIEW simple_view AS
SELECT id, name, salary
FROM employees;

UPDATE simple_view SET salary = 70000 WHERE id = 1;
```

#### Read-Only Views
- Views that involve complex queries (e.g., `JOIN`, `GROUP BY`, `DISTINCT`) or derived columns are read-only.

**Example**:
```sql
CREATE VIEW summary_view AS
SELECT department, AVG(salary) AS avg_salary
FROM employees
GROUP BY department;

-- This will fail as the view is read-only
UPDATE summary_view SET avg_salary = 75000 WHERE department = 'HR';
```

---

### **Benefits of Using Views**

1. **Data Abstraction**: Hide complexity of base table structures from users.
2. **Reusability**: Encapsulate common queries into reusable views.
3. **Data Security**: Expose only the required data to users, restricting access to sensitive columns or rows.
4. **Ease of Maintenance**: Centralize query logic in views, reducing redundancy.

---

### **Limitations of Views**

1. **Performance Overhead**:
   - Views are re-executed dynamically, which may impact performance for complex queries.
2. **Cannot Include Indexes**:
   - Views do not support indexes directly.
3. **Read-Only Restrictions**:
   - Some views cannot be updated or modified.

---

### **Analyzing Views**

#### View Definition
To see the definition of a view:
```sql
SHOW CREATE VIEW view_name;
```

**Example**:
```sql
SHOW CREATE VIEW hr_employees;
```

#### Check Existing Views
List all views in the database:
```sql
SHOW FULL TABLES WHERE TABLE_TYPE = 'VIEW';
```

---

### 🔥 **Summary**

| **Operation**        | **Command**                                                                 |
|-----------------------|---------------------------------------------------------------------------|
| **Create a View**     | `CREATE VIEW view_name AS SELECT ...;`                                   |
| **Query a View**      | `SELECT * FROM view_name;`                                               |
| **Modify a View**     | `CREATE OR REPLACE VIEW view_name AS SELECT ...;`                        |
| **Delete a View**     | `DROP VIEW view_name;`                                                  |
| **Check Definition**  | `SHOW CREATE VIEW view_name;`                                           |
| **List All Views**    | `SHOW FULL TABLES WHERE TABLE_TYPE = 'VIEW';`                           |


















****

****


















****
****

