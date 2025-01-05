

Here are the tables based on your updated request:

### **Login Table** (For User Authentication)

| Column Name     | Data Type    | Description                                      |
|-----------------|--------------|--------------------------------------------------|
| `username`      | `VARCHAR(255)`| Unique identifier for the user (username)       |
| `password_hash` | `VARCHAR(255)`| Hashed password for user authentication         |
| `role`          | `VARCHAR(50)` | User role (can be `vendor` or `customer` - hidden from the user in the login flow) |

---

### **Register Table** (For User Registration)

| Column Name     | Data Type    | Description                                      |
|-----------------|--------------|--------------------------------------------------|
| `username`      | `VARCHAR(255)`| Unique identifier for the user (username)       |
| `email`         | `VARCHAR(255)`| User email address                               |
| `password_hash` | `VARCHAR(255)`| Hashed password for user registration           |
| `created_at`    | `DATETIME`   | Timestamp when the user account was created     |
| `role`          | `VARCHAR(50)` | User role (defaults to `customer`, can be set to `vendor` by admin/vendor) - hidden |


Here is the updated schema with an added **Visibility** column to specify whether a field is accessible by **Customers**, **Vendors**, or both:

---

### **1. Products Table**

| **Column Name**                   | **Data Type**       | **Nullable?** | **Visibility**      | **Description**                                                                 |
|-----------------------------------|---------------------|---------------|---------------------|---------------------------------------------------------------------------------|
| `_id`                             | INT PRIMARY KEY     | No            | Customer & Vendor   | Unique identifier for the product.                                             |
| `name`                            | VARCHAR(255)        | No            | Customer & Vendor   | Name of the product.                                                           |
| `category_id`                     | INT                 | Yes           | Customer & Vendor   | ID of the category the product belongs to.                                     |
| `vendor_id`                       | INT                 | Yes           | Vendor Only         | ID of the vendor managing the product.                                         |
| `expenditure_cost_inr`            | DECIMAL(10, 2)      | Yes           | Vendor Only         | Fixed cost to purchase/manufacture the product.                                |
| `selling_price_inr`               | DECIMAL(10, 2)      | No            | Vendor Only         | Price of the product before any discount.                                      |
| `discount_percentage`             | DECIMAL(5, 2)       | Yes           | Customer & Vendor   | Discount percentage applied to the product.                                    |
| `after_discount_selling_price_inr`| DECIMAL(10, 2)      | Yes           | Customer & Vendor   | Selling price after applying the discount.                                     |
| `profit_per_item_inr`             | DECIMAL(10, 2)      | Yes           | Vendor Only         | Profit per item after deducting expenditure cost.                              |
| `stock_remaining`                 | INT                 | No            | Customer & Vendor   | Remaining stock available for sale.                                            |
| `image_url`                       | VARCHAR(255)        | Yes           | Customer & Vendor   | URL of the product image.                                                      |
| `description`                     | TEXT                | Yes           | Customer & Vendor   | Detailed description of the product.                                           |
| `created_at`                      | DATETIME            | No            | Vendor Only         | Timestamp when the product was created.                                        |
| `last_updated`                    | DATETIME            | No            | Vendor Only         | Timestamp when the product was last updated.                                   |

---

### **2. Categories Table**

| **Column Name**                   | **Data Type**       | **Nullable?** | **Visibility**      | **Description**                                                                 |
|-----------------------------------|---------------------|---------------|---------------------|---------------------------------------------------------------------------------|
| `category_id`                     | INT PRIMARY KEY     | No            | Customer & Vendor   | Unique identifier for the category.                                            |
| `name`                            | VARCHAR(255)        | No            | Customer & Vendor   | Name of the category.                                                          |
| `products`                        | JSON                | Yes           | Customer & Vendor   | List of product IDs in the category.                                           |

---

### **3. Stock Table**

| **Column Name**                   | **Data Type**       | **Nullable?** | **Visibility**      | **Description**                                                                 |
|-----------------------------------|---------------------|---------------|---------------------|---------------------------------------------------------------------------------|
| `product_id`                      | INT PRIMARY KEY     | No            | Vendor Only         | Unique identifier for the product.                                             |
| `total_stock`                     | INT                 | No            | Vendor Only         | Total initial stock available.                                                 |
| `stock_remaining`                 | INT                 | No            | Customer & Vendor   | Remaining stock after orders.                                                  |
| `total_stock_price_inr`           | DECIMAL(15, 2)      | Yes           | Vendor Only         | Total value of remaining stock based on expenditure cost.                      |
| `last_updated`                    | DATETIME            | No            | Vendor Only         | Timestamp of the last stock update.                                            |

---

### **4. Orders Table**

| **Column Name**                   | **Data Type**       | **Nullable?** | **Visibility**      | **Description**                                                                 |
|-----------------------------------|---------------------|---------------|---------------------|---------------------------------------------------------------------------------|
| `order_id`                        | INT PRIMARY KEY     | No            | Customer & Vendor   | Unique identifier for the order.                                               |
| `customer_id`                     | INT                 | No            | Vendor Only         | ID of the customer who placed the order.                                       |
| `vendor_id`                       | INT                 | Yes           | Vendor Only         | ID of the vendor fulfilling the order.                                         |
| `order_date`                      | DATETIME            | No            | Customer & Vendor   | Timestamp when the order was placed.                                           |
| `status`                          | VARCHAR(50)         | No            | Customer & Vendor   | Current status of the order (e.g., Pending, Processing, Delivered).            |
| `items`                           | JSON                | No            | Customer & Vendor   | List of products with quantities in the order.                                 |
| `total_amount_inr`                | DECIMAL(15, 2)      | No            | Customer & Vendor   | Total amount for the order in INR.                                             |
| `total_profit_inr`                | DECIMAL(15, 2)      | Yes           | Vendor Only         | Total profit from delivered products in the order.                             |
| `processed_by`                    | INT                 | Yes           | Vendor Only         | ID of the vendor who processed the order.                                      |
| `processed_at`                    | DATETIME            | Yes           | Vendor Only         | Timestamp when the order was processed.                                        |
| `delivered_at`                    | DATETIME            | Yes           | Customer & Vendor   | Timestamp when the order was delivered.                                        |

---

### **5. Vendors Authentication Table**

| **Column Name**                   | **Data Type**       | **Nullable?** | **Visibility**      | **Description**                                                                 |
|-----------------------------------|---------------------|---------------|---------------------|---------------------------------------------------------------------------------|
| `vendor_id`                       | INT PRIMARY KEY     | No            | Vendor Only         | Unique identifier for the vendor.                                              |
| `vendor_name`                     | VARCHAR(255)        | No            | Vendor Only         | Name of the vendor.                                                            |
| `email`                           | VARCHAR(255) UNIQUE | No            | Vendor Only         | Email address of the vendor.                                                   |
| `password_hash`                   | VARCHAR(255)        | No            | Vendor Only         | Hashed password for secure authentication.                                     |
| `created_at`                      | DATETIME            | No            | Vendor Only         | Timestamp of registration.                                                     |

---

### **6. Customers Authentication Table**

| **Column Name**                   | **Data Type**       | **Nullable?** | **Visibility**      | **Description**                                                                 |
|-----------------------------------|---------------------|---------------|---------------------|---------------------------------------------------------------------------------|
| `customer_id`                     | INT PRIMARY KEY     | No            | Vendor Only         | Unique identifier for the customer.                                            |
| `username`                        | VARCHAR(255) UNIQUE | No            | Customer & Vendor   | Username chosen by the customer.                                               |
| `email`                           | VARCHAR(255) UNIQUE | No            | Vendor Only         | Email address of the customer.                                                 |
| `password_hash`                   | VARCHAR(255)        | No            | Vendor Only         | Hashed password for secure authentication.                                     |
| `created_at`                      | DATETIME            | No            | Vendor Only         | Timestamp of registration.                                                     |

---

### **7. Cart Table**

| **Column Name**                   | **Data Type**       | **Nullable?** | **Visibility**      | **Description**                                                                 |
|-----------------------------------|---------------------|---------------|---------------------|---------------------------------------------------------------------------------|
| `cart_id`                         | INT PRIMARY KEY     | No            | Customer & Vendor   | Unique identifier for the cart.                                                |
| `customer_id`                     | INT                 | No            | Vendor Only         | ID of the customer who owns the cart.                                          |
| `items`                           | JSON                | Yes           | Customer & Vendor   | List of products with quantities in the cart.                                  |
| `cart_total_inr`                  | DECIMAL(15, 2)      | Yes           | Customer & Vendor   | Total value of the cart in INR.                                                |

---

### **8. Wishlist Table**

| **Column Name**                   | **Data Type**       | **Nullable?** | **Visibility**      | **Description**                                                                 |
|-----------------------------------|---------------------|---------------|---------------------|---------------------------------------------------------------------------------|
| `wishlist_id`                     | INT PRIMARY KEY     | No            | Customer & Vendor   | Unique identifier for the wishlist.                                            |
| `customer_id`                     | INT                 | No            | Vendor Only         | ID of the customer who owns the wishlist.                                      |
| `product_id`                      | INT                 | No            | Customer & Vendor   | ID of the product in the wishlist.                                             |
| `product_name`                    | VARCHAR(255)        | No            | Customer & Vendor   | Name of the product.                                                           |
| `price_inr`                       | DECIMAL(15, 2)      | Yes           | Customer & Vendor   | Price of the product in INR.                                                   |

---

### **9. Reviews Table**

| **Column Name**                   | **Data Type**       | **Nullable?** | **Visibility**      | **Description**                                                                 |
|-----------------------------------|---------------------|---------------|---------------------|---------------------------------------------------------------------------------|
| `review_id`                       | INT PRIMARY KEY     | No            | Customer & Vendor   | Unique identifier for the review.                                              |
| `product_id`                      | INT                 | No            | Customer & Vendor   | ID of the product being reviewed.                                              |
| `customer_id`                     | INT                 | No            | Vendor Only         | ID of the customer who left the review.                                        |
| `rating`                          | DECIMAL(2, 1)       | No            | Customer & Vendor   | Rating for the product (1–5).                                                  |
| `comment`                         | TEXT                | Yes           | Customer & Vendor   | Customer's comment about the product.                                          |
| `timestamp`                       | DATETIME            | No            | Customer & Vendor   | Timestamp when the review was created.                                         |

---

### **10. Payments Table**

| **Column Name**                   | **Data Type**       | **Nullable?** | **Visibility**      | **Description**                                                                 |
|-----------------------------------|---------------------|---------------|---------------------|---------------------------------------------------------------------------------|
| `payment_id`                      | INT PRIMARY KEY     | No            | Customer & Vendor   | Unique identifier for the payment.                                             |
| `order_id`                        | INT                 | No            | Customer & Vendor   | ID of the order for which payment is made.                                     |
| `customer_id`                     | INT                 | No            | Vendor Only         | ID of the customer making the payment.                                         |
| `amount_paid_inr`                 | DECIMAL(15, 2)      | No            | Customer & Vendor   | Total amount paid for the order.                                               |
| `payment_method`                  | VARCHAR(50)         | No            | Customer & Vendor   | Payment method (e.g., Credit Card, UPI, Net Banking).                          |
| `transaction_id`                  | VARCHAR(255)        | No            | Customer & Vendor   | Unique identifier for the payment transaction.                                 |
| `status`                          | VARCHAR(50)         | No            | Customer & Vendor   | Status of the payment (e.g., Pending, Completed, Failed).                      |
| `payment_date`                    | DATETIME            | No            | Customer & Vendor   | Timestamp when the payment was made.                                           |

---

This updated schema now includes the **Visibility** column to clarify field access for **Customers** and **Vendors**.
