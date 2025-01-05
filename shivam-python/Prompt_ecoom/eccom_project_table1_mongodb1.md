# Ecommerce :

### **1. Register Collection**

| **Field Name**  | **Data Type** | **Nullability** | **Description**                                       |
|------------------|---------------|-----------------|-------------------------------------------------------|
| `_id`           | `ObjectId`    | Not Nullable    | Auto-generated unique ID for the user.               |
| `username`      | `String`      | Not Nullable    | Unique username for the user.                        |
| `email`         | `String`      | Not Nullable    | User email address (unique).                         |
| `password_hash` | `String`      | Not Nullable    | Hashed password for user registration.               |
| `role`          | `String`      | Not Nullable    | User role (e.g., `vendor` or `customer`).            |
| `created_at`    | `Date`        | Not Nullable    | Timestamp when the user account was created.         |

---

### **2. Login Collection**

| **Field Name**  | **Data Type** | **Nullability** | **Description**                                       |
|------------------|---------------|-----------------|-------------------------------------------------------|
| `_id`           | `ObjectId`    | Not Nullable    | Auto-generated unique ID for the login session.      |
| `user_id`       | `ObjectId`    | Not Nullable    | Reference to the user in the Register collection.    |
| `username`      | `String`      | Not Nullable    | Username for the user (used for login).              |
| `password_hash` | `String`      | Not Nullable    | Hashed password for user authentication.             |
| `role`          | `String`      | Not Nullable    | User role (hidden at frontend).                      |

---


### **3. Products Collection**

| **Field Name**                     | **Data Type**     | **Nullability** | **Visibility**       | **Description**                                       |
|-------------------------------------|-------------------|-----------------|----------------------|-------------------------------------------------------|
| `_id`                              | `ObjectId`        | Not Nullable    | Customer & Vendor    | Auto-generated unique ID.                            |
| `name`                             | `String`          | Not Nullable    | Customer & Vendor    | Product name.                                         |
| `category_id`                      | `ObjectId`        | Nullable        | Customer & Vendor    | Reference to the category.                           |
| `user_id`                          | `ObjectId`        | Not Nullable    | Customer & Vendor    | Reference to the vendor managing the product.        |
| `expenditure_cost_inr`             | `NumberDecimal`   | Nullable        | Vendor Only          | Cost to produce/manufacture.                         |
| `selling_price_inr`                | `NumberDecimal`   | Not Nullable    | Vendor Only          | Selling price before discount.                       |
| `discount_percentage`              | `NumberDecimal`   | Nullable        | Customer & Vendor    | Discount percentage.                                 |
| `after_discount_selling_price_inr` | `NumberDecimal`   | Nullable        | Customer & Vendor    | Price after discount.                                |
| `profit_per_item_inr`              | `NumberDecimal`   | Nullable        | Vendor Only          | Profit per item after cost.                          |
| `stock_remaining`                  | `NumberInt`       | Not Nullable    | Customer & Vendor    | Remaining stock.                                     |
| `image_url`                        | `String`          | Nullable        | Customer & Vendor    | URL of product image.                                |
| `description`                      | `String`          | Nullable        | Customer & Vendor    | Product description.                                 |
| `created_at`                       | `Date`            | Not Nullable    | Vendor Only          | Creation timestamp.                                  |
| `last_updated`                     | `Date`            | Not Nullable    | Vendor Only          | Last update timestamp.                               |

---

### **4. Categories Collection**

| **Field Name**     | **Data Type**  | **Nullability** | **Visibility**       | **Description**                         |
|---------------------|---------------|-----------------|----------------------|-----------------------------------------|
| `_id`              | `ObjectId`    | Not Nullable    | Customer & Vendor    | Auto-generated unique ID.              |
| `name`             | `String`      | Not Nullable    | Customer & Vendor    | Name of the category.                  |
| `products`         | `Array<ObjectId>` | Nullable    | Customer & Vendor    | Array of product IDs in the category.  |

---

### **5. Stock Collection**

| **Field Name**         | **Data Type**     | **Nullability** | **Visibility**       | **Description**                               |
|-------------------------|-------------------|-----------------|----------------------|-----------------------------------------------|
| `_id`                  | `ObjectId`        | Not Nullable    | Vendor Only          | Auto-generated unique ID.                    |
| `product_id`           | `ObjectId`        | Not Nullable    | Vendor Only          | Reference to the product.                    |
| `user_id`              | `ObjectId`        | Not Nullable    | Vendor Only          | Reference to the vendor managing the stock.  |
| `total_stock`          | `NumberInt`       | Not Nullable    | Vendor Only          | Total initial stock.                         |
| `stock_remaining`      | `NumberInt`       | Not Nullable    | Customer & Vendor    | Remaining stock after orders.                |
| `total_stock_price_inr`| `NumberDecimal`   | Nullable        | Vendor Only          | Total value of remaining stock.              |
| `last_updated`         | `Date`            | Not Nullable    | Vendor Only          | Timestamp of the last stock update.          |

---

### **6. Orders Collection**

| **Field Name**         | **Data Type**     | **Nullability** | **Visibility**       | **Description**                               |
|-------------------------|-------------------|-----------------|----------------------|-----------------------------------------------|
| `_id`                  | `ObjectId`        | Not Nullable    | Customer & Vendor    | Auto-generated unique ID.                    |
| `user_id`              | `ObjectId`        | Not Nullable    | Customer & Vendor    | Reference to the customer placing the order. |
| `vendor_id`            | `ObjectId`        | Nullable        | Vendor Only          | Reference to the vendor fulfilling the order.|
| `order_date`           | `Date`            | Not Nullable    | Customer & Vendor    | Timestamp when the order was placed.         |
| `status`               | `String`          | Not Nullable    | Customer & Vendor    | Order status (Pending, Delivered, etc.).     |
| `items`                | `Array`           | Not Nullable    | Customer & Vendor    | List of products with quantities in the order.|
| `total_amount_inr`     | `NumberDecimal`   | Not Nullable    | Customer & Vendor    | Total amount for the order.                  |
| `processed_at`         | `Date`            | Nullable        | Vendor Only          | Timestamp when the order was processed.      |
| `delivered_at`         | `Date`            | Nullable        | Customer & Vendor    | Timestamp when the order was delivered.      |

---

### **7. Cart Collection**

| **Field Name**       | **Data Type**     | **Nullability** | **Visibility**       | **Description**                               |
|-----------------------|-------------------|-----------------|----------------------|-----------------------------------------------|
| `_id`                | `ObjectId`        | Not Nullable    | Customer Only        | Auto-generated unique ID.                    |
| `user_id`            | `ObjectId`        | Not Nullable    | Customer Only        | Reference to the customer owning the cart.   |
| `items`              | `Array`           | Nullable        | Customer Only        | List of products with quantities in the cart.|
| `cart_total_inr`     | `NumberDecimal`   | Nullable        | Customer Only        | Total value of the cart.                     |

---

### **8. Wishlist Collection**

| **Field Name**       | **Data Type**     | **Nullability** | **Visibility**       | **Description**                               |
|-----------------------|-------------------|-----------------|----------------------|-----------------------------------------------|
| `_id`                | `ObjectId`        | Not Nullable    | Customer Only        | Auto-generated unique ID.                    |
| `user_id`            | `ObjectId`        | Not Nullable    | Customer Only        | Reference to the customer owning the wishlist.|
| `products`           | `Array`           | Nullable        | Customer Only        | Array of product details:                    |
|                       | - `product_id`   | `ObjectId`      | Nullable             | Product ID.                                  |
|                       | - `product_name` | `String`        | Nullable             | Product name.                                |
|                       | - `price_inr`    | `NumberDecimal` | Nullable             | Price of the product.                        |

---

### **9. Reviews Collection**

| **Field Name**       | **Data Type**     | **Nullability** | **Visibility**       | **Description**                               |
|-----------------------|-------------------|-----------------|----------------------|-----------------------------------------------|
| `_id`                | `ObjectId`        | Not Nullable    | Customer Only        | Auto-generated unique ID.                    |
| `product_id`         | `ObjectId`        | Not Nullable    | Customer Only        | Reference to the product being reviewed.     |
| `user_id`            | `ObjectId`        | Not Nullable    | Customer Only        | Reference to the customer leaving the review.|
| `rating`             | `NumberDecimal`   | Not Nullable    | Customer Only        | Rating for the product (1–5).                |
| `comment`            | `String`          | Nullable        | Customer Only        | Review comment.                              |
| `timestamp`          | `Date`            | Not Nullable    | Customer Only        | Timestamp when the review was created.       |

---

### **10. Payments Collection**

| **Field Name**        | **Data Type**     | **Nullability** | **Visibility**       | **Description**                               |
|------------------------|-------------------|-----------------|----------------------|-----------------------------------------------|
| `_id`                 | `ObjectId`        | Not Nullable    | Customer Only        | Auto-generated unique ID.                    |
| `order_id`            | `ObjectId`        | Not Nullable    | Customer Only        | Reference to the order.                      |
| `user_id`             | `ObjectId`        | Not Nullable    | Customer Only        | Reference to the customer making payment.    |
| `amount_paid_inr`     | `NumberDecimal`   | Not Nullable    | Customer Only        | Total amount paid.                           |
| `payment_method`      | `String`          | Not Nullable    | Customer Only        | Payment method (e.g., Credit Card, UPI).     |
| `transaction_id`      | `String`          | Not Nullable    | Customer Only        | Unique transaction ID.                       |
| `status`              | `String`          | Not Nullable    | Customer Only        | Payment status (Pending, Completed, etc.).   |
| `payment_date`        | `Date`            | Not Nullable    | Customer Only        | Timestamp when payment was made.             |

---

