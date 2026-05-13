# 🏭 B2B Wholesale Platform (PHP)

A complete PHP-based platform that connects **factories**, **wholesalers**, and **retailers** in one system.  
Factories add products, wholesalers buy in bulk, and retailers order smaller quantities with online payment.

This project demonstrates real-world experience in building multi-role systems, order management, and e‑commerce logic using **pure PHP + MySQL**.

---
## 📸 Screenshots

### 🏠 Dashboard
<p align="center">
  <img src="https://github.com/maheraldarra2/b2b-wholesale-platform/blob/main/1.jpeg" width="750">
</p>

### 🛍️ Products Page
<p align="center">
  <img src="https://github.com/maheraldarra2/b2b-wholesale-platform/blob/main/2.jpeg" width="750">
</p>

### 📦 Orders Management
<p align="center">
  <img src="https://github.com/maheraldarra2/b2b-wholesale-platform/blob/main/3.jpeg" width="750">
</p>

### 💳 Checkout / Payment
<p align="center">
  <img src="https://github.com/maheraldarra2/b2b-wholesale-platform/blob/main/4.jpeg" width="750">
</p>


## 👥 User Roles

### 🏭 Factory
- Add products  
- Set wholesale & retail prices  
- Manage stock  
- View and approve orders from wholesalers  

### 🧺 Wholesaler
- Browse factory products  
- Place bulk orders  
- Sell to retailers  
- Manage orders  

### 🛒 Retailer
- Browse products from wholesalers  
- Add items to cart  
- Place small orders  
- Pay online  

---

## ✨ Features

- Role-based authentication (Factory / Wholesaler / Retailer)  
- Product catalog with categories and filters  
- Cart system  
- Order management (pending → approved → shipped → completed)  
- Online payment integration (PayPal / Paymob)  
- Image upload for products  
- Stock management  
- Dashboards for each user type  
- Clean and simple UI  

---

## 🧰 Tech Stack

- **PHP Native** (No framework)  
- **MySQL**  
- **HTML / CSS / JavaScript**  
- **PayPal / Paymob API**  
- **Bootstrap** (optional)

---

## 🗄️ Database Structure

### `users`
- id  
- name  
- email  
- password  
- role (factory / wholesaler / retailer)  
- created_at  

### `products`
- id  
- factory_id  
- name  
- description  
- price_factory  
- price_wholesale  
- price_retail  
- stock  
- image  
- created_at  

### `orders`
- id  
- user_id  
- total_price  
- status  
- created_at  

### `order_items`
- id  
- order_id  
- product_id  
- quantity  
- price  

---

## 📦 Project Structure

/public
index.php
login.php
register.php
products.php
cart.php
checkout.php

/factory
dashboard.php
add_product.php
orders.php

/wholesaler
dashboard.php
orders.php

/retailer
dashboard.php
orders.php

/includes
db.php
auth.php
header.php
footer.php

/uploads
product_images/

---

## 🔧 Installation

1. Import the SQL file into MySQL  
2. Configure database connection in `/includes/db.php`  
3. Place the project inside `htdocs` (XAMPP) or your hosting  
4. Open in browser:  

---

## 💳 Payment Integration

Supports:  
- **PayPal Checkout**  
- **Paymob** (recommended for Middle East)

---

## 📬 Contact

For questions or improvements:  
**GitHub:** https://github.com/maheraldarra2  
