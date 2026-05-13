# B2B Wholesale Platform

A web platform that connects factories, wholesalers, and retailers in one place.  
Factories can list products, wholesalers can buy in bulk, and retailers can order smaller quantities with online payments.

---

## 👥 User Roles

- **Factories:** Add products, set wholesale prices, manage stock, view and approve orders.  
- **Wholesalers:** Browse factory products, place bulk orders, resell to retailers.  
- **Retailers:** Browse products from wholesalers, place smaller orders, and pay online.

---

## 🧰 Tech Stack

- Laravel (PHP)
- MySQL
- Blade / Bootstrap
- Payment Gateway (PayPal / Paymob)

---

## 🚀 Core Features

- Role-based authentication (Factory / Wholesaler / Retailer)  
- Product catalog with categories and filters  
- Cart and order management  
- Online payment integration  
- Dashboards for each user type  
- Order status tracking

---

## 📦 Setup (Development)

1. Clone the repository  
2. Run `composer install`  
3. Copy `.env.example` to `.env` and configure database  
4. Run `php artisan key:generate`  
5. Run migrations: `php artisan migrate`  
6. Start server: `php artisan serve`
