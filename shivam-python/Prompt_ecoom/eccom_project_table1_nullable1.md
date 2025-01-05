

---

### **1. Register Table** (For User Registration)

| **Column Name**   | **Data Type**         | **Description**                                         |
|-------------------|-----------------------|---------------------------------------------------------|
| `user_id`         | INT PRIMARY KEY AUTO_INCREMENT | Unique identifier for the user (can be seen by both).   |
| `username`        | `VARCHAR(255)`       | Unique identifier for the user (username).              |
| `email`           | `VARCHAR(255)`       | User email address (must be unique).                    |
| `password_hash`   | `VARCHAR(255)`       | Hashed password for user registration.                  |
| `role`            | `VARCHAR(50)`        | User role (`vendor` or default `customer`, handled by DB).|
| `created_at`      | `DATETIME`           | Timestamp when the user account was created.            |

---

### **2. Login Table** (For User Authentication)

| **Column Name**   | **Data Type**    | **Description**                                     |
|-------------------|------------------|-----------------------------------------------------|
| `user_id`         | INT              | Unique identifier for the user (can be seen by both). |
| `username`        | `VARCHAR(255)`  | Unique identifier for the user (username).          |
| `password_hash`   | `VARCHAR(255)`  | Hashed password for user authentication.            |
| `role`            | `VARCHAR(50)`   | - **Hidden at UI frontend** - User role (`vendor` or `customer`). |

---

### **3. Products Table**

| **Column Name**                     | **Data Type**       | **Nullability** | **Visibility**     | **Description**                                                                 |
|-------------------------------------|---------------------|-----------------|--------------------|---------------------------------------------------------------------------------|
| `product_id`                        | INT PRIMARY KEY     | NOT NULL        | Customer & Vendor  | Unique identifier for the product.                                             |
| `name`                              | VARCHAR(255)        | NOT NULL        | Customer & Vendor  | Name of the product.                                                           |
| `category_id`                       | INT                 | NULL            | Customer & Vendor  | ID of the category the product belongs to.                                     |
| `user_id`                           | INT                 | NOT NULL        | Customer & Vendor  | Common `user_id` of the vendor managing the product.                           |
| `expenditure_cost_inr`              | DECIMAL(10, 2)      | NULL            | Vendor Only        | Fixed cost to purchase/manufacture the product.                                |
| `selling_price_inr`                 | DECIMAL(10, 2)      | NOT NULL        | Vendor Only        | Price of the product before any discount.                                      |
| `discount_percentage`               | DECIMAL(5, 2)       | NULL            | Customer & Vendor  | Discount percentage applied to the product.                                    |
| `after_discount_selling_price_inr`  | DECIMAL(10, 2)      | NULL            | Customer & Vendor  | Selling price after applying the discount.                                     |
| `profit_per_item_inr`               | DECIMAL(10, 2)      | NULL            | Vendor Only        | Profit per item after deducting expenditure cost.                              |
| `stock_remaining`                   | INT                 | NOT NULL        | Customer & Vendor  | Remaining stock available for sale.                                            |
| `image_url`                         | VARCHAR(255)        | NULL            | Customer & Vendor  | URL of the product image.                                                      |
| `description`                       | TEXT                | NULL            | Customer & Vendor  | Detailed description of the product.                                           |
| `created_at`                        | DATETIME            | NOT NULL        | Vendor Only        | Timestamp when the product was created.                                        |
| `last_updated`                      | DATETIME            | NOT NULL        | Vendor Only        | Timestamp when the product was last updated.                                   |

---

### **4. Categories Table**

| **Column Name**                     | **Data Type**       | **Nullability** | **Visibility**     | **Description**                                                                 |
|-------------------------------------|---------------------|-----------------|--------------------|---------------------------------------------------------------------------------|
| `category_id`                       | INT PRIMARY KEY     | NOT NULL        | Customer & Vendor  | Unique identifier for the category.                                            |
| `name`                              | VARCHAR(255)        | NOT NULL        | Customer & Vendor  | Name of the category.                                                          |
| `products`                          | JSON                | NULL            | Customer & Vendor  | List of product IDs in the category.                                           |

---

### **5. Stock Table**

| **Column Name**                     | **Data Type**       | **Nullability** | **Visibility**     | **Description**                                                                 |
|-------------------------------------|---------------------|-----------------|--------------------|---------------------------------------------------------------------------------|
| `product_id`                        | INT PRIMARY KEY     | NOT NULL        | Vendor Only        | Unique identifier for the product.                                             |
| `user_id`                           | INT                 | NOT NULL        | Customer & Vendor  | Common `user_id` of the vendor managing the stock.                             |
| `total_stock`                       | INT                 | NOT NULL        | Vendor Only        | Total initial stock available.                                                 |
| `stock_remaining`                   | INT                 | NOT NULL        | Customer & Vendor  | Remaining stock after orders.                                                  |
| `total_stock_price_inr`             | DECIMAL(15, 2)      | NULL            | Vendor Only        | Total value of remaining stock based on expenditure cost.                      |
| `last_updated`                      | DATETIME            | NOT NULL        | Vendor Only        | Timestamp of the last stock update.                                            |

---

### **6. Orders Table**

| **Column Name**                     | **Data Type**       | **Nullability** | **Visibility**     | **Description**                                                                 |
|-------------------------------------|---------------------|-----------------|--------------------|---------------------------------------------------------------------------------|
| `order_id`                          | INT PRIMARY KEY     | NOT NULL        | Customer & Vendor  | Unique identifier for the order.                                               |
| `user_id`                           | INT                 | NOT NULL        | Customer & Vendor  | Common `user_id` of the customer placing the order.                            |
| `vendor_id`                         | INT                 | NULL            | Vendor Only        | Common `user_id` of the vendor fulfilling the order.                           |
| `order_date`                        | DATETIME            | NOT NULL        | Customer & Vendor  | Timestamp when the order was placed.                                           |
| `status`                            | VARCHAR(50)         | NOT NULL        | Customer & Vendor  | Current status of the order (Pending, Delivered, etc.).                        |
| `items`                             | JSON                | NOT NULL        | Customer & Vendor  | List of products with quantities in the order.                                 |
| `total_amount_inr`                  | DECIMAL(15, 2)      | NOT NULL        | Customer & Vendor  | Total amount for the order in INR.                                             |
| `processed_at`                      | DATETIME            | NULL            | Vendor Only        | Timestamp when the order was processed.                                        |
| `delivered_at`                      | DATETIME            | NULL            | Customer & Vendor  | Timestamp when the order was delivered.                                        |

---

### **7. Cart Table**

| **Column Name**                     | **Data Type**       | **Nullability** | **Visibility**     | **Description**                                                                 |
|-------------------------------------|---------------------|-----------------|--------------------|---------------------------------------------------------------------------------|
| `cart_id`                           | INT PRIMARY KEY     | NOT NULL        | Customer Only      | Unique identifier for the cart.                                                |
| `user_id`                           | INT                 | NOT NULL        | Customer & Vendor  | Common `user_id` of the customer owning the cart.                              |
| `items`                             | JSON                | NULL            | Customer Only      | List of products with quantities in the cart.                                  |
| `cart_total_inr`                    | DECIMAL(15, 2)      | NULL            | Customer Only      | Total value of the cart in INR.                                                |

---

### **8. Wishlist Table**

| **Column Name**                     | **Data Type**       | **Nullability** | **Visibility**     | **Description**                                                                 |
|-------------------------------------|---------------------|-----------------|--------------------|---------------------------------------------------------------------------------|
| `wishlist_id`                       | INT PRIMARY KEY     | NOT NULL        | Customer Only      | Unique identifier for the wishlist.                                            |
| `user_id`                           | INT                 | NOT NULL        | Customer & Vendor  | Common `user_id` of the customer owning the wishlist.                          |
| `product_id`                        | INT                 | NOT NULL        | Customer Only      | ID of the product in the wishlist.                                             |
| `product_name`                      | VARCHAR(255)        | NOT NULL        | Customer Only      | Name of the product.                                                           |
| `price_inr`                         | DECIMAL(15, 2)      | NULL            | Customer Only      | Price of the product in INR.                                                   |

---

### **9. Reviews Table**

| **Column Name**                     | **Data Type**       | **Nullability** | **Visibility**     | **Description**                                                                 |
|-------------------------------------|---------------------|-----------------|--------------------|---------------------------------------------------------------------------------|
| `review_id`                         | INT PRIMARY KEY     | NOT NULL        | Customer Only      | Unique identifier for the review.                                              |
| `product_id`                        | INT                 | NOT NULL        | Customer Only      | ID of the product being reviewed.                                              |
| `user_id`                           | INT                 | NOT NULL        | Customer & Vendor  | Common `user_id` of the customer leaving the review.                           |
| `rating`                            | DECIMAL(2, 1)       | NOT NULL        | Customer Only      | Rating for the product (1–5).                                                  |
| `comment`                           | TEXT                | NULL            | Customer Only      | Customer's comment about the product.                                          |
| `timestamp`                         | DATETIME            | NOT NULL        | Customer Only      | Timestamp when the review was created.                                         |

---

### **10. Payments Table**

| **Column Name**                     | **Data Type**       | **Nullability** | **Visibility**     | **Description**                                                                 |
|-------------------------------------|---------------------|-----------------|--------------------|---------------------------------------------------------------------------------|
| `payment_id`                        | INT PRIMARY KEY     | NOT NULL        | Customer Only      | Unique identifier for the payment.                                             |
| `order_id`                          | INT                 | NOT NULL        | Customer Only      | ID of the order for which payment is made.                                     |
| `user_id`                           | INT                 | NOT NULL        | Customer & Vendor  | Common `user_id` of the customer making the payment.                           |
| `amount_paid_inr`                   | DECIMAL(15, 2)      | NOT NULL        | Customer Only      | Total amount paid for the order.                                               |
| `payment_method`                    | VARCHAR(50)         | NOT NULL        | Customer Only      | Payment method (e.g., Credit Card, UPI, Net Banking).                          |
| `transaction_id`                    | VARCHAR(255)        | NOT NULL        | Customer Only      | Unique identifier for the payment transaction.                                 |
| `status`                            | VARCHAR(50)         | NOT NULL        | Customer Only      | Status of the payment (Pending, Completed, Failed).                            |
| `payment_date`                      | DATETIME            | NOT NULL        | Customer Only      | Timestamp when the payment was made.                                           |

---


