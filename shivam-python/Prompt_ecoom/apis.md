
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
    "name": "Product A",
    "category_id": 1,
    "selling_price_inr": 300,
    "expenditure_cost_inr": 200,
    "discount_percentage": 10,
    "total_stock": 100,
    "stock_remaining": 80,
    "image_url": "http://example.com/product-a.jpg",
    "description": "This is Product A"
}

Get : http://127.0.0.1:5000/api/products

[
    {
        "_id": 1,
        "after_discount_selling_price_inr": 270.0,
        "category_id": 1,
        "created_at": "Mon, 06 Jan 2025 09:24:19 GMT",
        "description": "This is Product A",
        "discount_percentage": 10,
        "expenditure_cost_inr": 200,
        "image_url": "http://example.com/product-a.jpg",
        "last_updated": "Mon, 06 Jan 2025 09:28:11 GMT",
        "name": "Product A",
        "profit_per_item_inr": 70.0,
        "selling_price_inr": 300,
        "stock_remaining": 78,
        "total_stock": 100,
        "total_stock_price_inr": 21060.0,
        "user_id": 1
    }
]

Post : http://127.0.0.1:5000/api/cart/add

{
    "product_id": 1,
    "quantity": 2
}

Get : http://127.0.0.1:5000/api/cart/
Put : http://127.0.0.1:5000/api/cart/update
Delete : http://127.0.0.1:5000/api/cart/remove/1
Delete : http://127.0.0.1:5000/api/cart/clear

Post : http://127.0.0.1:5000/api/wishlist/add
{
    "product_id": 1
}
Delete : http://127.0.0.1:5000/api/wishlist/clear

Post : http://127.0.0.1:5000/api/orders/create

{
    "message": "Order created successfully.",
    "order_id": 1
}

Get : http://127.0.0.1:5000/api/orders/

---

/components/Navbar.jsx
/components/Login.jsx
/components/Logout.jsx
/components/Register.jsx
/components/Profile.jsx
/components/ProductList.jsx
/components/api.js
App.jsx
-- frontend using vite http://localhost:5173/



```
