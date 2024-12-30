
















### **MySQL Interview Questions**  


---

### **Basic Level MySQL Interview Questions**  

1. **What is MySQL?**  
2. **Explain the differences between MySQL and SQL.**  
3. **What are the key features of MySQL?**  
4. **What are the different data types in MySQL?**  
5. **What is a primary key in MySQL?**  
6. **What is the difference between `CHAR` and `VARCHAR`?**  
7. **What are the common MySQL storage engines?**  
8. **What is the default port number for MySQL?**  
9. **How do you create a database in MySQL?**  
10. **What is the difference between `DELETE`, `TRUNCATE`, and `DROP`?**  
11. **What is a foreign key in MySQL?**  
12. **What is the difference between `UNION` and `UNION ALL`?**  
13. **What are constraints in MySQL?**  
14. **What is indexing in MySQL?**  
15. **What is the difference between a clustered and a non-clustered index?**  
16. **How do you retrieve the structure of a table in MySQL?**  
17. **What is a default value in a column?**  
18. **What is normalization, and what are its different forms?**  
19. **What is denormalization?**  
20. **How do you start and stop the MySQL server?**  

---

### **Intermediate Level MySQL Interview Questions**  

1. **What is a MySQL transaction?**  
2. **Explain the ACID properties in MySQL.**  
3. **What is the difference between `WHERE` and `HAVING` clauses?**  
4. **What are stored procedures in MySQL?**  
5. **How do you create and call a stored procedure?**  
6. **What are triggers in MySQL?**  
7. **What is the difference between `NOW()` and `CURRENT_DATE()`?**  
8. **What is a view in MySQL, and why is it used?**  
9. **Explain the difference between `INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`, and `FULL JOIN`.**  
10. **What is a composite key in MySQL?**  
11. **How does MySQL handle indexing for large datasets?**  
12. **What is the difference between `BLOB` and `TEXT`?**  
13. **What is the purpose of the `LIMIT` clause?**  
14. **What is the difference between `IS NULL` and `= NULL`?**  
15. **What are MySQL functions, and how are they different from stored procedures?**  
16. **What is the purpose of the `IN` and `EXISTS` clauses?**  
17. **How do you optimize a slow query in MySQL?**  
18. **What are temporary tables in MySQL?**  
19. **What is the difference between `MyISAM` and `InnoDB` storage engines?**  
20. **What is the use of the `EXPLAIN` statement in MySQL?**  

---

### **Advanced Level MySQL Interview Questions**  

1. **What are the different types of joins supported in MySQL?**  
2. **Explain the architecture of MySQL.**  
3. **What is the Query Optimizer in MySQL?**  
4. **What are subqueries, and how are they used in MySQL?**  
5. **What are the differences between a correlated subquery and a non-correlated subquery?**  
6. **What is the purpose of the `GROUP BY` clause?**  
7. **What is replication in MySQL, and what are its types?**  
8. **What are the differences between master-slave and master-master replication?**  
9. **What are MySQL partitions, and how do they work?**  
10. **What is the difference between horizontal and vertical scaling in MySQL?**  
11. **How does MySQL handle deadlocks?**  
12. **What is the difference between `ROW` and `STATEMENT` binary log formats in MySQL?**  
13. **What are foreign key constraints, and how are they enforced in MySQL?**  
14. **How does MySQL ensure data security?**  
15. **What are full-text searches in MySQL?**  
16. **What is the difference between `MERGE` and `UNION` in MySQL?**  
17. **How does MySQL handle concurrent updates on the same row?**  
18. **What are MySQL performance schema and its use cases?**  
19. **What is MySQL clustering, and how does it differ from replication?**  
20. **How do you back up and restore MySQL databases?**  

---

### **Scenario-Based MySQL Questions**  

1. **How would you design a schema for an e-commerce application in MySQL?**  
2. **How would you optimize a MySQL database for read-heavy workloads?**  
3. **How would you troubleshoot a slow-running query?**  
4. **How would you handle a situation where a MySQL table becomes too large?**  
5. **How would you design a database for a social media application in MySQL?**  
6. **How would you implement a leaderboard system using MySQL?**  
7. **How would you migrate data from a MySQL database to another database?**  
8. **How would you set up master-slave replication in MySQL?**  
9. **What steps would you take to ensure database security?**  
10. **How would you handle schema changes in a live database?**  

---

### **Best Practices and Optimization Questions**  

1. **What are the best practices for indexing in MySQL?**  
2. **How do you monitor and tune MySQL performance?**  
3. **What are the anti-patterns in MySQL schema design?**  
4. **How do you secure a MySQL database?**  
5. **What tools are available for MySQL monitoring and management?**  
6. **What are the benefits of partitioning in MySQL?**  
7. **What are the common pitfalls to avoid in MySQL query optimization?**  
8. **How do you handle high availability in MySQL?**  
9. **What are the best practices for writing complex queries in MySQL?**  
10. **What strategies would you use to ensure data integrity in MySQL?**  

---

### **Practical Query Questions**  

1. **Write a query to find the second-highest salary in an employee table.**  
2. **Write a query to fetch all employees whose names start with 'A'.**  
3. **Write a query to update the salary of employees in the IT department by 10%.**  
4. **Write a query to delete duplicate rows in a table.**  
5. **Write a query to display the department-wise highest salary of employees.**  
6. **Write a query to fetch the names of employees hired in the last 30 days.**  
7. **Write a query to join two tables and fetch matching rows.**  
8. **Write a query to find the total revenue grouped by product in a sales table.**  
9. **Write a query to create a stored procedure for calculating factorials.**  
10. **Write a query to implement pagination using the `LIMIT` clause.**  

---

****
****
****
****
****
****


# Indexing 

### **50 SQL Interview Questions on Indexing**

Indexing is a critical concept in SQL for database performance optimization. Below is a list of interview questions exclusively focused on indexing, covering basic, intermediate, and advanced aspects.

---

### **Basic Level Questions**

1. **What is an index in SQL?**
2. **What are the benefits of using indexes in SQL?**
3. **What are the different types of indexes in SQL?**
4. **What is the difference between a clustered and non-clustered index?**
5. **What is the primary key index in SQL?**
6. **Can a table have more than one index?**
7. **What are the drawbacks of using indexes?**
8. **What is the difference between a unique index and a primary key index?**
9. **How do indexes affect INSERT, UPDATE, and DELETE operations?**
10. **What is the syntax to create an index in SQL?**

    ```sql
    CREATE INDEX index_name ON table_name (column_name);
    ```

11. **What is the difference between a composite index and a single-column index?**
12. **How does SQL automatically create indexes on certain constraints?**
13. **What is the difference between implicit and explicit indexing?**
14. **What is a bitmap index?**
15. **What is the syntax for creating a unique index?**

    ```sql
    CREATE UNIQUE INDEX index_name ON table_name (column_name);
    ```

16. **What happens if an index becomes fragmented?**
17. **Can an index be created on a computed column?**
18. **How do you drop an index in SQL?**

    ```sql
    DROP INDEX index_name;
    ```

19. **What is the maximum number of indexes a table can have?**
20. **Can indexes be created on views?**

---

### **Intermediate Level Questions**

21. **What is a covering index in SQL?**
22. **What is a filtered index, and when should you use it?**
23. **What is a full-text index, and how is it different from a regular index?**
24. **What is the difference between a clustered index and a heap?**
25. **What are descending indexes, and why are they used?**
26. **What is index maintenance, and why is it important?**
27. **What is an index hint in SQL, and how do you use it?**

    ```sql
    SELECT * FROM table_name WITH (INDEX (index_name)) WHERE condition;
    ```

28. **What is index selectivity, and how does it impact query performance?**
29. **What are the best practices for choosing columns to index?**
30. **What is index cardinality?**
31. **What is an index scan, and how does it differ from a table scan?**
32. **What is an index seek, and how does it improve query performance?**
33. **What is the difference between a partial index and a full index?**
34. **How does an index impact database locking and blocking?**
35. **What are the pros and cons of indexing foreign key columns?**
36. **Can you create an index on a column that allows NULL values?**
37. **What is the purpose of the `REBUILD` and `REORGANIZE` options for indexes?**

    ```sql
    ALTER INDEX index_name ON table_name REBUILD;
    ALTER INDEX index_name ON table_name REORGANIZE;
    ```

38. **What is the difference between a B-tree index and a hash index?**
39. **How do indexes affect the execution plan of a query?**
40. **What is the difference between dense and sparse indexes?**

---

### **Advanced Level Questions**

41. **What are the considerations for indexing large tables?**
42. **How does indexing affect the performance of OLTP and OLAP systems differently?**
43. **What are invisible indexes, and how do they work?**
44. **What is the impact of indexed views on query performance?**
45. **What are the advantages and disadvantages of unique indexes?**
46. **What is a spatial index, and how is it used in geospatial queries?**
47. **How do you monitor index usage in a database?**
48. **How can index fragmentation be detected and resolved?**
49. **What is the difference between index compression and page compression?**
50. **How do columnstore indexes differ from rowstore indexes?**

---

### **Additional Scenario-Based Questions**

- **How would you optimize a query that involves sorting a large dataset?**
- **Which index would you use for a high cardinality column, and why?**
- **How do you decide which columns to include in a composite index?**
- **If a query is running slow even with an index, what steps would you take to investigate?**
- **How do you handle indexing in a table that undergoes frequent writes?**































---

****
****
****
****
****
****













