Here’s the complete updated schema for all the tables, considering nullable fields and refined attributes based on your requirements.

---

### **1. Products Table**

| **Column Name**                   | **Data Type**       | **Nullable?** | **Description**                                                                 |
|-----------------------------------|---------------------|---------------|---------------------------------------------------------------------------------|
| `_id`                             | INT PRIMARY KEY     | No            | Unique identifier for the product.                                             |
| `name`                            | VARCHAR(255)        | No            | Name of the product.                                                           |
| `category_id`                     | INT                 | Yes           | ID of the category the product belongs to.                                     |
| `vendor_id`                       | INT                 | Yes           | ID of the vendor managing the product.                                         |
| `expenditure_cost_inr`            | DECIMAL(10, 2)      | Yes           | Fixed cost to purchase/manufacture the product.                                |
| `selling_price_inr`               | DECIMAL(10, 2)      | No            | Price of the product before any discount.                                      |
| `discount_percentage`             | DECIMAL(5, 2)       | Yes           | Discount percentage applied to the product.                                    |
| `after_discount_selling_price_inr`| DECIMAL(10, 2)      | Yes           | Selling price after applying the discount.                                     |
| `profit_per_item_inr`             | DECIMAL(10, 2)      | Yes           | Profit per item after deducting expenditure cost.                              |
| `stock_remaining`                 | INT                 | No            | Remaining stock available for sale.                                            |
| `image_url`                       | VARCHAR(255)        | Yes           | URL of the product image.                                                      |
| `description`                     | TEXT                | Yes           | Detailed description of the product.                                           |
| `created_at`                      | DATETIME            | No            | Timestamp when the product was created.                                        |
| `last_updated`                    | DATETIME            | No            | Timestamp when the product was last updated.                                   |

---

### **2. Categories Table**

| **Column Name**                   | **Data Type**       | **Nullable?** | **Description**                                                                 |
|-----------------------------------|---------------------|---------------|---------------------------------------------------------------------------------|
| `category_id`                     | INT PRIMARY KEY     | No            | Unique identifier for the category.                                            |
| `name`                            | VARCHAR(255)        | No            | Name of the category.                                                          |
| `products`                        | JSON                | Yes           | List of product IDs in the category.                                           |

---

### **3. Stock Table**

| **Column Name**                   | **Data Type**       | **Nullable?** | **Description**                                                                 |
|-----------------------------------|---------------------|---------------|---------------------------------------------------------------------------------|
| `product_id`                      | INT PRIMARY KEY     | No            | Unique identifier for the product.                                             |
| `total_stock`                     | INT                 | No            | Total initial stock available.                                                 |
| `stock_remaining`                 | INT                 | No            | Remaining stock after orders.                                                  |
| `total_stock_price_inr`           | DECIMAL(15, 2)      | Yes           | Total value of remaining stock based on expenditure cost.                      |
| `last_updated`                    | DATETIME            | No            | Timestamp of the last stock update.                                            |

---

### **4. Orders Table**

| **Column Name**                   | **Data Type**       | **Nullable?** | **Description**                                                                 |
|-----------------------------------|---------------------|---------------|---------------------------------------------------------------------------------|
| `order_id`                        | INT PRIMARY KEY     | No            | Unique identifier for the order.                                               |
| `customer_id`                     | INT                 | No            | ID of the customer who placed the order.                                       |
| `vendor_id`                       | INT                 | Yes           | ID of the vendor fulfilling the order.                                         |
| `order_date`                      | DATETIME            | No            | Timestamp when the order was placed.                                           |
| `status`                          | VARCHAR(50)         | No            | Current status of the order (e.g., Pending, Processing, Delivered).            |
| `items`                           | JSON                | No            | List of products with quantities in the order.                                 |
| `total_amount_inr`                | DECIMAL(15, 2)      | No            | Total amount for the order in INR.                                             |
| `total_profit_inr`                | DECIMAL(15, 2)      | Yes           | Total profit from delivered products in the order.                             |
| `processed_by`                    | INT                 | Yes           | ID of the vendor who processed the order.                                      |
| `processed_at`                    | DATETIME            | Yes           | Timestamp when the order was processed.                                        |
| `delivered_at`                    | DATETIME            | Yes           | Timestamp when the order was delivered.                                        |

---

### **5. Vendors Authentication Table**

| **Column Name**                   | **Data Type**       | **Nullable?** | **Description**                                                                 |
|-----------------------------------|---------------------|---------------|---------------------------------------------------------------------------------|
| `vendor_id`                       | INT PRIMARY KEY     | No            | Unique identifier for the vendor.                                              |
| `vendor_name`                     | VARCHAR(255)        | No            | Name of the vendor.                                                            |
| `email`                           | VARCHAR(255) UNIQUE | No            | Email address of the vendor.                                                   |
| `password_hash`                   | VARCHAR(255)        | No            | Hashed password for secure authentication.                                     |
| `created_at`                      | DATETIME            | No            | Timestamp of registration.                                                     |

---

### **6. Customers Authentication Table**

| **Column Name**                   | **Data Type**       | **Nullable?** | **Description**                                                                 |
|-----------------------------------|---------------------|---------------|---------------------------------------------------------------------------------|
| `customer_id`                     | INT PRIMARY KEY     | No            | Unique identifier for the customer.                                            |
| `username`                        | VARCHAR(255) UNIQUE | No            | Username chosen by the customer.                                               |
| `email`                           | VARCHAR(255) UNIQUE | No            | Email address of the customer.                                                 |
| `password_hash`                   | VARCHAR(255)        | No            | Hashed password for secure authentication.                                     |
| `created_at`                      | DATETIME            | No            | Timestamp of registration.                                                     |

---

### **7. Cart Table**

| **Column Name**                   | **Data Type**       | **Nullable?** | **Description**                                                                 |
|-----------------------------------|---------------------|---------------|---------------------------------------------------------------------------------|
| `cart_id`                         | INT PRIMARY KEY     | No            | Unique identifier for the cart.                                                |
| `customer_id`                     | INT                 | No            | ID of the customer who owns the cart.                                          |
| `items`                           | JSON                | Yes           | List of products with quantities in the cart.                                  |
| `cart_total_inr`                  | DECIMAL(15, 2)      | Yes           | Total value of the cart in INR.                                                |

---

### **8. Wishlist Table**

| **Column Name**                   | **Data Type**       | **Nullable?** | **Description**                                                                 |
|-----------------------------------|---------------------|---------------|---------------------------------------------------------------------------------|
| `wishlist_id`                     | INT PRIMARY KEY     | No            | Unique identifier for the wishlist.                                            |
| `customer_id`                     | INT                 | No            | ID of the customer who owns the wishlist.                                      |
| `product_id`                      | INT                 | No            | ID of the product in the wishlist.                                             |
| `product_name`                    | VARCHAR(255)        | No            | Name of the product.                                                           |
| `price_inr`                       | DECIMAL(15, 2)      | Yes           | Price of the product in INR.                                                   |

---

### **9. Reviews Table**

| **Column Name**                   | **Data Type**       | **Nullable?** | **Description**                                                                 |
|-----------------------------------|---------------------|---------------|---------------------------------------------------------------------------------|
| `review_id`                       | INT PRIMARY KEY     | No            | Unique identifier for the review.                                              |
| `product_id`                      | INT                 | No            | ID of the product being reviewed.                                              |
| `customer_id`                     | INT                 | No            | ID of the customer who left the review.                                        |
| `rating`                          | DECIMAL(2, 1)       | No            | Rating for the product (1–5).                                                  |
| `comment`                         | TEXT                | Yes           | Customer's comment about the product.                                          |
| `timestamp`                       | DATETIME            | No            | Timestamp when the review was created.                                         |

---

### **10. Payments Table**

| **Column Name**                   | **Data Type**       | **Nullable?** | **Description**                                                                 |
|-----------------------------------|---------------------|---------------|---------------------------------------------------------------------------------|
| `payment_id`                      | INT PRIMARY KEY     | No            | Unique identifier for the payment.                                             |
| `order_id`                        | INT                 | No            | ID of the order for which payment is made.                                     |
| `customer_id`                     | INT                 | No            | ID of the customer making the payment.                                         |
| `amount_paid_inr`                 | DECIMAL(15, 2)      | No            | Total amount paid for the order.                                               |
| `payment_method`                  | VARCHAR(50)         | No            | Payment method (e.g., Credit Card, UPI, Net Banking).                          |
| `transaction_id`                  | VARCHAR(255)        | No            | Unique identifier for the payment transaction.                                 |
| `status`                          | VARCHAR(50)         | No            | Status of the payment (e.g., Pending, Completed, Failed).                      |
| `payment_date`                    | DATETIME            | No            | Timestamp when the payment was made.                                           |

---

This structure ensures flexibility and clarity while adhering to your requirements.