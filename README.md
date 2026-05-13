https://mandob.de/
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
1) User Registration & Login
   - The user opens the platform.
   - Selects account type (Factory / Wholesaler / Retailer).
   - Registers a new account or logs in.
   - The system redirects the user to the appropriate dashboard based on their role.

2) Factory Flow
   - Accesses the Factory Dashboard.
   - Adds new products (name, description, prices, stock, image).
   - Views incoming wholesale orders from wholesalers.
   - Approves or rejects orders.
   - Order status is updated for the wholesaler.

3) Wholesaler Flow
   - Accesses the Wholesaler Dashboard.
   - Browses products added by factories.
   - Adds items to the cart in bulk quantities.
   - Creates a new order.
   - Waits for factory approval.
   - After approval, can resell products to retailers.

4) Retailer Flow
   - Accesses the Retailer Dashboard.
   - Browses products from wholesalers.
   - Adds items to the cart in small quantities.
   - Proceeds to online payment (PayPal / Paymob).
   - Places the order.
   - Tracks order status (Pending → Approved → Shipped → Completed).

5) Order Processing Flow
   - User creates an order.
   - System generates Order + Order Items.
   - Order is sent to the appropriate party (Factory or Wholesaler).
   - Receiver approves or rejects the order.
   - Stock is updated upon approval.
   - Order status is updated for the user.

6) Payment Flow
   - User selects online payment.
   - Redirected to the payment gateway.
   - After successful payment, user is redirected back.
   - Order is confirmed and status updated.
The system is built using a modular PHP architecture with clear separation between
presentation, business logic, and data layers. The platform consists of four main
components: Frontend, Backend (Core PHP Logic), Database, and Payment Gateway.

- Built using HTML, CSS, JavaScript, and Bootstrap.
- Provides separate dashboards for each user role (Factory, Wholesaler, Retailer).
- Handles product browsing, cart interactions, order creation, and payment redirection.
- Communicates with backend PHP scripts through standard HTTP requests (POST/GET).

- Pure PHP (no framework) structured into modules.
- Contains all business logic for authentication, product management, order processing,
  stock updates, and role-based access control.
- Uses include-based modular structure (db.php, auth.php, controllers, helpers).

- Stores all persistent data: users, products, orders, order items.
- Uses relational structure with foreign keys to maintain data integrity.
- Designed to support multi-role interactions between factories, wholesalers, and retailers.

- Integrates external payment providers (PayPal / Paymob).
- Frontend redirects user to the payment gateway.
- After successful payment, the gateway returns the user to a callback URL.
- Backend verifies the payment and updates the order status.

Frontend → sends request → Backend PHP → interacts with Database → returns response → Frontend updates UI

User → Checkout → Payment Gateway → Callback → Backend verifies → Order confirmed

Frontend (UI/UX)
   ↓
Backend (PHP Logic)
   ↓
Database (MySQL)
   ↓
Payment Gateway (PayPal / Paymob)

## 🗄️ Database Structure
[ USERS ]
- id (PK)
- name
- email
- password
- role (factory / wholesaler / retailer)

        1 ───────────────< ∞

[ PRODUCTS ]
- id (PK)
- factory_id (FK → users.id)
- name
- description
- price_factory
- price_wholesale
- price_retail
- stock
- image

        1 ───────────────< ∞

[ ORDERS ]
- id (PK)
- user_id (FK → users.id)
- total_price
- status (pending / approved / shipped / completed)

        1 ───────────────< ∞

[ ORDER_ITEMS ]
- id (PK)
- order_id (FK → orders.id)
- product_id (FK → products.id)
- quantity
- price


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
