Here’s a comprehensive list of MongoDB interview questions covering basic to advanced levels, categorized for clarity:

---

### **Basic MongoDB Interview Questions**

1. **What is MongoDB?**
   - MongoDB is a NoSQL database that uses a document-oriented data model. It stores data in flexible, JSON-like documents.

2. **What are the key features of MongoDB?**
   - Schema-less (or flexible schema)
   - High performance and scalability
   - Rich query language
   - Index support
   - Aggregation framework
   - Replication and Sharding for high availability and scalability.

3. **Explain the difference between MongoDB and a relational database.**
   - MongoDB is schema-less, while relational databases have a fixed schema.
   - MongoDB uses documents and collections, whereas relational databases use tables and rows.
   - Joins are not directly supported in MongoDB.

4. **What is a document in MongoDB?**
   - A document is a record in MongoDB stored in a JSON-like format (BSON internally).

5. **What is a collection in MongoDB?**
   - A collection is a group of MongoDB documents, equivalent to a table in relational databases.

6. **What is BSON?**
   - BSON (Binary JSON) is a binary representation of JSON-like documents, optimized for storage and data traversal in MongoDB.

7. **How do you start the MongoDB server?**
   - Use the `mongod` command to start the MongoDB server.

8. **What are the primary data types in MongoDB?**
   - String, Integer, Boolean, Array, Object, Date, ObjectId, Binary Data, etc.

9. **What is the default port for MongoDB?**
   - The default port is `27017`.

10. **What is a primary key in MongoDB?**
    - Every document must have a unique `_id` field, which acts as the primary key.

---

### **Intermediate MongoDB Interview Questions**

11. **What is sharding in MongoDB?**
    - Sharding is the process of distributing data across multiple servers to handle large datasets and ensure high availability.

12. **What is replication in MongoDB?**
    - Replication involves copying data across multiple servers to provide data redundancy and high availability.

13. **What is a replica set?**
    - A replica set is a group of MongoDB servers that maintain the same dataset, ensuring redundancy and fault tolerance.

14. **What is the Aggregation Framework in MongoDB?**
    - It is used for performing complex data transformations and computations on the server side. Common stages include `$match`, `$group`, `$sort`, `$project`.

15. **What is an index in MongoDB?**
    - An index is a special data structure that improves query performance by allowing faster retrieval of documents.

16. **Explain the difference between a capped collection and a normal collection.**
    - A capped collection is a fixed-size collection that maintains insertion order and automatically overwrites the oldest documents when the size limit is reached.

17. **What is GridFS in MongoDB?**
    - GridFS is a specification for storing and retrieving large files, like images or videos, in smaller chunks.

18. **What is the use of the `$lookup` operator?**
    - The `$lookup` operator is used to perform joins between collections.

19. **What is a covered query in MongoDB?**
    - A query is considered covered when all the fields in the query and returned results are part of an index.

20. **Explain the difference between `find()` and `findOne()`.**
    - `find()` retrieves all documents matching the query criteria, while `findOne()` retrieves only the first document.

---

### **Advanced MongoDB Interview Questions**

21. **What are the differences between MongoDB and Cassandra?**
    - MongoDB: Document-oriented, supports rich queries, schema-less.
    - Cassandra: Column-family oriented, optimized for write-heavy workloads.

22. **What are the write concerns in MongoDB?**
    - Write concerns determine the level of acknowledgment requested from MongoDB for write operations:
      - `w`: Number of nodes acknowledging the write.
      - `j`: Journaling acknowledgment.
      - `wtimeout`: Timeout for write acknowledgment.

23. **What is the difference between horizontal and vertical scaling in MongoDB?**
    - Horizontal scaling involves adding more servers (sharding), while vertical scaling involves increasing the resources (CPU, RAM) of a single server.

24. **How does MongoDB handle transactions?**
    - MongoDB supports multi-document transactions (introduced in version 4.0), ensuring ACID compliance.

25. **Explain the working of the WiredTiger storage engine.**
    - WiredTiger provides compression and document-level concurrency for efficient storage and faster access.

26. **What are TTL indexes in MongoDB?**
    - TTL (Time-to-Live) indexes are special indexes that automatically remove documents from a collection after a specified period.

27. **What is the difference between `aggregate()` and `mapReduce()`?**
    - `aggregate()` is the preferred method for data aggregation due to performance and simplicity, while `mapReduce()` offers more flexibility but is slower.

28. **How can you back up and restore MongoDB data?**
    - Use the `mongodump` and `mongorestore` utilities to back up and restore data.

29. **How does MongoDB ensure consistency and availability in a distributed environment?**
    - MongoDB uses replica sets for consistency and sharding for scalability and availability.

30. **What is the difference between `$in` and `$nin` in MongoDB?**
    - `$in`: Matches documents where the field's value is in the specified array.
    - `$nin`: Matches documents where the field's value is not in the specified array.

---

### **Scenario-Based MongoDB Questions**

31. **How would you design a schema for a social media platform in MongoDB?**
    - Discuss using collections for users, posts, comments, and likes with proper relationships and embedding where necessary.

32. **How would you optimize a MongoDB query?**
    - Use indexes, limit the returned fields with projections, and analyze the query using `explain()`.

33. **How would you implement a search feature in MongoDB?**
    - Use text indexes for full-text search and `$text` operator for querying.

34. **What steps would you take to handle a large dataset in MongoDB?**
    - Implement sharding, indexing, and use appropriate schema design (embedding vs referencing).

35. **How do you handle concurrency in MongoDB?**
    - Use locking mechanisms (MongoDB has collection-level and document-level locking) and write concerns to ensure data consistency.

---

### **Practical MongoDB Query Questions**

36. **Write a query to fetch all users aged 25 or older.**
    ```javascript
    db.users.find({ age: { $gte: 25 } })
    ```

37. **Write a query to update the salary of all employees in the IT department by 10%.**
    ```javascript
    db.employees.updateMany(
      { department: "IT" },
      { $mul: { salary: 1.1 } }
    )
    ```

38. **Write a query to delete all records older than 30 days.**
    ```javascript
    db.records.deleteMany({ createdAt: { $lt: new Date(new Date() - 30 * 24 * 60 * 60 * 1000) } })
    ```

39. **Write a query to find all employees whose names start with "A".**
    ```javascript
    db.employees.find({ name: { $regex: "^A", $options: "i" } })
    ```

40. **Write an aggregation pipeline to group sales data by product and calculate the total revenue.**
    ```javascript
    db.sales.aggregate([
      { $group: { _id: "$product", totalRevenue: { $sum: "$amount" } } }
    ])
    ```

****
****
****
****
****
****

















