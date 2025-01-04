Here’s the **complete updated schema**, including the changes for order processing and delivery by vendors:

---

### **1. Products Table**
| **Column Name**                     | **Data Type**       | **Visibility**      | **Description**                                                    |
|-------------------------------------|---------------------|---------------------|--------------------------------------------------------------------|
| `product_id`                        | INT PRIMARY KEY     | Customer & Vendor   | Unique identifier for the product.                                 |
| `name`                              | VARCHAR(255)        | Customer & Vendor   | Name of the product.                                               |
| `category_id`                       | INT                 | Customer & Vendor   | ID of the category the product belongs to.                         |
| `vendor_id`                         | INT                 | Vendor Only         | ID of the vendor managing the product.                             |
| `expenditure_cost_inr`              | DECIMAL(10, 2)      | Vendor Only         | Fixed cost to purchase/manufacture the product.                    |
| `selling_price_inr`                 | DECIMAL(10, 2)      | Vendor Only         | Price of the product before any discount.                          |
| `discount_percentage`               | DECIMAL(5, 2)       | Customer & Vendor   | Discount percentage applied to the product.                        |
| `after_discount_selling_price_inr`  | DECIMAL(10, 2)      | Customer & Vendor   | Selling price after applying the discount.                         |
| `profit_per_item_inr`               | DECIMAL(10, 2)      | Vendor Only         | Profit per item after deducting expenditure cost.                  |
| `image_url`                         | VARCHAR(255)        | Customer & Vendor   | URL of the product image.                                          |
| `description`                       | TEXT                | Customer & Vendor   | Detailed description of the product.                               |
| `created_at`                        | DATETIME            | Vendor Only         | Timestamp when the product was created.                            |
| `last_updated`                      | DATETIME            | Vendor Only         | Timestamp when the product was last updated.                       |

---

### **2. Categories Table**
| **Column Name**                     | **Data Type**       | **Visibility**      | **Description**                                                    |
|-------------------------------------|---------------------|---------------------|--------------------------------------------------------------------|
| `category_id`                       | INT PRIMARY KEY     | Customer & Vendor   | Unique identifier for the category.                                |
| `name`                              | VARCHAR(255)        | Customer & Vendor   | Name of the category.                                              |
| `products`                          | JSON                | Customer & Vendor   | List of product IDs in the category.                               |

---

### **3. Stock Table**
| **Column Name**                     | **Data Type**       | **Visibility**      | **Description**                                                    |
|-------------------------------------|---------------------|---------------------|--------------------------------------------------------------------|
| `product_id`                        | INT PRIMARY KEY     | Vendor Only         | Unique identifier for the product.                                 |
| `total_stock`                       | INT                 | Vendor Only         | Total initial stock available.                                     |
| `stock_remaining`                   | INT                 | Customer & Vendor   | Remaining stock after orders.                                      |
| `total_stock_price_inr`             | DECIMAL(15, 2)      | Vendor Only         | Total value of remaining stock based on expenditure cost.          |
| `last_updated`                      | DATETIME            | Vendor Only         | Timestamp of the last stock update.                                |

---

### **4. Orders Table**
| **Column Name**                     | **Data Type**       | **Visibility**      | **Description**                                                    |
|-------------------------------------|---------------------|---------------------|--------------------------------------------------------------------|
| `order_id`                          | INT PRIMARY KEY     | Customer & Vendor   | Unique identifier for the order.                                   |
| `customer_id`                       | INT                 | Vendor Only         | ID of the customer who placed the order.                           |
| `vendor_id`                         | INT                 | Vendor Only         | ID of the vendor fulfilling the order.                             |
| `order_date`                        | DATETIME            | Customer & Vendor   | Timestamp when the order was placed.                               |
| `status`                            | VARCHAR(50)         | Customer & Vendor   | Current status of the order (e.g., Pending, Processing, Delivered).|
| `items`                             | JSON                | Customer & Vendor   | List of products with quantities in the order.                     |
| `units_delivered`                   | INT                 | Vendor Only         | Number of units delivered for each product.                        |
| `total_amount_inr`                  | DECIMAL(15, 2)      | Customer & Vendor   | Total amount for the order in INR.                                 |
| `total_profit_inr`                  | DECIMAL(15, 2)      | Vendor Only         | Total profit from delivered products in the order.                 |
| `processed_by`                      | INT                 | Vendor Only         | ID of the vendor who processed the order.                          |
| `processed_at`                      | DATETIME            | Vendor Only         | Timestamp when the order was processed.                            |
| `delivered_at`                      | DATETIME            | Customer & Vendor   | Timestamp when the order was delivered.                            |

---

### **5. Vendors Authentication Table**
| **Column Name**                     | **Data Type**       | **Visibility**      | **Description**                                                    |
|-------------------------------------|---------------------|---------------------|--------------------------------------------------------------------|
| `vendor_id`                         | INT PRIMARY KEY     | Vendor Only         | Unique identifier for the vendor.                                  |
| `vendor_name`                       | VARCHAR(255)        | Vendor Only         | Name of the vendor.                                                |
| `email`                             | VARCHAR(255) UNIQUE | Vendor Only         | Email address of the vendor.                                       |
| `password_hash`                     | VARCHAR(255)        | Vendor Only         | Hashed password for secure authentication.                         |
| `created_at`                        | DATETIME            | Vendor Only         | Timestamp of registration.                                         |

---

### **6. Customers Authentication Table**
| **Column Name**                     | **Data Type**       | **Visibility**      | **Description**                                                    |
|-------------------------------------|---------------------|---------------------|--------------------------------------------------------------------|
| `customer_id`                       | INT PRIMARY KEY     | Vendor Only         | Unique identifier for the customer.                                |
| `username`                          | VARCHAR(255) UNIQUE | Customer & Vendor   | Username chosen by the customer.                                   |
| `email`                             | VARCHAR(255) UNIQUE | Vendor Only         | Email address of the customer.                                     |
| `password_hash`                     | VARCHAR(255)        | Vendor Only         | Hashed password for secure authentication.                         |
| `created_at`                        | DATETIME            | Vendor Only         | Timestamp of registration.                                         |

---

### **7. Cart Table**
| **Column Name**                     | **Data Type**       | **Visibility**      | **Description**                                                    |
|-------------------------------------|---------------------|---------------------|--------------------------------------------------------------------|
| `cart_id`                           | INT PRIMARY KEY     | Customer & Vendor   | Unique identifier for the cart.                                    |
| `customer_id`                       | INT                 | Vendor Only         | ID of the customer who owns the cart.                              |
| `items`                             | JSON                | Customer & Vendor   | List of products with quantities in the cart.                      |
| `cart_total_inr`                    | DECIMAL(15, 2)      | Customer & Vendor   | Total value of the cart in INR.                                    |

---

### **8. Wishlist Table**
| **Column Name**                     | **Data Type**       | **Visibility**      | **Description**                                                    |
|-------------------------------------|---------------------|---------------------|--------------------------------------------------------------------|
| `wishlist_id`                       | INT PRIMARY KEY     | Customer & Vendor   | Unique identifier for the wishlist.                                |
| `customer_id`                       | INT                 | Vendor Only         | ID of the customer who owns the wishlist.                          |
| `product_id`                        | INT                 | Customer & Vendor   | ID of the product in the wishlist.                                 |
| `product_name`                      | VARCHAR(255)        | Customer & Vendor   | Name of the product.                                               |
| `price_inr`                         | DECIMAL(15, 2)      | Customer & Vendor   | Price of the product in INR.                                       |

---

### **9. Reviews Table**
| **Column Name**                     | **Data Type**       | **Visibility**      | **Description**                                                    |
|-------------------------------------|---------------------|---------------------|--------------------------------------------------------------------|
| `review_id`                         | INT PRIMARY KEY     | Customer & Vendor   | Unique identifier for the review.                                  |
| `product_id`                        | INT                 | Customer & Vendor   | ID of the product being reviewed.                                  |
| `customer_id`                       | INT                 | Vendor Only         | ID of the customer who left the review.                            |
| `rating`                            | DECIMAL(2, 1)       | Customer & Vendor   | Rating for the product (1–5).                                      |
| `comment`                           | TEXT                | Customer & Vendor   | Customer's comment about the product.                              |
| `timestamp`                         | DATETIME            | Customer & Vendor   | Timestamp when the review was created.                             |

---

Let me know if further details are needed!
