
```
Post: http://127.0.0.1:5000/api/auth/register

{
  "username": "user1",
  "password": "user1",
  "email": "user1@gmail.com",
  "role": "customer"
}

Post : http://127.0.0.1:5000/api/auth/login

{
  "username": "user1",
  "password": "user1"
}
Post : http://127.0.0.1:5000/api/auth/logout

Get : http://127.0.0.1:5000/api/auth/profile
{
    "_id": "1",
    "email": "user1@gmail.com",
    "role": "vendor",
    "username": "user1"
}
Post : http://127.0.0.1:5000/api/products

{
{
  "name": "Wireless Headphones",
  "category": "Electronics",
  "selling_price_inr": 3500,
  "discount_percentage": 12,
  "expenditure_cost_inr": 2500,
  "total_stock": 120,
  "description": "Noise-canceling wireless headphones with long battery life",
  "image_url": "http://example.com/wireless_headphones.jpg"
}

}

Get : http://127.0.0.1:5000/api/products

[
    {
        "_id": 31,
        "after_discount_selling_price_inr": 3080.0,
        "category": "Electronics",
        "created_at": "Tue, 14 Jan 2025 19:14:57 GMT",
        "description": "Noise-canceling wireless headphones with long battery life",
        "discount_percentage": 12,
        "expenditure_cost_inr": 2500,
        "image_url": "http://example.com/wireless_headphones.jpg",
        "last_updated": "Tue, 14 Jan 2025 19:14:57 GMT",
        "name": "Wireless Headphones",
        "profit_per_item_inr": 580.0,
        "selling_price_inr": 3500,
        "stock_remaining": 120,
        "total_stock": 120,
        "total_stock_price_inr": 369600.0,
        "user_id": 1
    }
]

Post : http://127.0.0.1:5000/api/auth/cart/add 

{
    "product_id": 1,
    "quantity": 2
}

Get : http://127.0.0.1:5000/api/auth/cart/ 
{
    "_id": 3,
    "created_at": "Sat, 11 Jan 2025 23:00:13 GMT",
    "items": [
        {
            "image_url": "http://example.com/product-a.jpg",
            "name": "Product A",
            "price": 270.0,
            "product_id": 1,
            "quantity": 15
        }
    ],
    "last_updated": "Sun, 12 Jan 2025 07:51:37 GMT",
    "user_id": 1
}
Put : http://127.0.0.1:5000/api/auth/cart/update
{
    "product_id": 1,
    "quantity": 5
}

Delete : http://127.0.0.1:5000/api/auth/cart/remove/<product_id>
Delete : http://127.0.0.1:5000/api/auth/cart/clear

Post : http://127.0.0.1:5000/api/auth/wishlist/add
{
    "product_id": 1
}

Delete : http://127.0.0.1:5000/api/auth/wishlist/clear

Post : http://127.0.0.1:5000/api/auth/orders/create-by-product

{
    "product_id": 1,
    "quantity": 2,
    "shipping_address": "123 Main Street, City, Country"
}
GET : http://127.0.0.1:5000/api/auth/wishlist/
{
    "products": []
}
Post : http://127.0.0.1:5000/api/auth/orders/create-from-cart
{
    "shipping_address": "123 Main Street, City, Country"
}
GET http://127.0.0.1:5000/api/auth/orders
[
    {
        "order_id": 101,
        "user_id": 1,
        "items": [
            {
                "product_id": 1,
                "name": "Product A",
                "quantity": 2,
                "price": 270.0
            }
        ],
        "total_price": 540.0,
        "shipping_address": "123 Main Street, City, Country",
        "created_at": "2025-01-12T08:30:00Z",
        "status": "Pending"
    },
    {
        "order_id": 102,
        "user_id": 1,
        "items": [
            {
                "product_id": 2,
                "name": "Product B",
                "quantity": 1,
                "price": 300.0
            }
        ],
        "total_price": 300.0,
        "shipping_address": "456 Main Avenue, City, Country",
        "created_at": "2025-01-13T09:15:00Z",
        "status": "Shipped"
    }
]

GET http://127.0.0.1:5000/api/orders/vendor
[
    {
        "order_id": 101,
        "customer_id": 1,
        "items": [
            {
                "product_id": 1,
                "name": "Product A",
                "quantity": 2,
                "price": 270.0
            }
        ],
        "total_price": 540.0,
        "shipping_address": "123 Main Street, City, Country",
        "created_at": "2025-01-12T08:30:00Z",
        "status": "Pending"
    }
]

PUT http://127.0.0.1:5000/api/orders/vendor/<order_id>
{
    "status": "Shipped"
}

---
/components/Home.jsx
/components/Navbar.jsx with Home, Products, Login, Register, if Loggined `Logout`
/components/Login.jsx with Register Logout button

/components/Register.jsx with Login Logout button
/components/Profile.jsx Loggined user
/components/ProductList.jsx no need login
/components/Cart.jsx - with user_id , loggined user
/components/Wishlist.jsx with user_id, loggined user
AuthContext.jsx
api.js
App.jsx
-- frontend using vite http://localhost:5173/



```
```


backend/
├── models/
│   ├── cart.py
│   ├── email.py
│   ├── order.py
│   ├── payment.py
│   ├── product.py
│   ├── review.py
│   ├── user.py
│   ├── util.py
│   ├── wishlist.py
├── routes/
│   ├── auth_routes.py
│   ├── cart_routes.py
│   ├── order_routes.py
│   ├── payment_routes.py
│   ├── product_routes.py
│   ├── review_routes.py
│   ├── wishlist_routes.py
├── venv/
├── .env
├── .gitignore
├── app.py
├── config.py
├── extensions.py
├── requirements.txt





```
