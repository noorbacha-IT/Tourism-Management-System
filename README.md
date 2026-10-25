# Tourism-Management-System

A Java desktop application for managing a travel and tourism business — tour packages, hotel bookings, customers and payments — built with Java Swing, JDBC and MySQL.

# 🌍 Tourism Management System – Java Desktop Application

Tourism Management System helps a travel company manage its customers, tour packages, hotels and bookings from one place. Customers can register, browse tour packages and hotels, book them, see the total cost and pay, while the admin manages customers and creates new tour packages. All data is stored in a centralised MySQL database, replacing slow manual record-keeping with a fast, user-friendly system.

🎥 **Demo video:** [Watch on YouTube](https://youtu.be/V5Kx1NTVZw0)

---

## 🚀 Features

### 🔹 Authentication & Account Security
- Separate **Admin** and **Customer** login portals
- Sign-up with a security question and answer
- **Forgot Password** recovery through the security question
- Login and sign-up queries use **parameterised `PreparedStatement`s**
- Input validation on every form (mandatory fields, invalid username/password alerts)

### 🔹 Customer Module
- Register customer details (CNIC/ID, gender, country, address, phone, email)
- Browse **Bronze, Silver and Gold** tour packages with included services and prices
- Book a package with **automatic price calculation** per number of persons
- View booked package details

### 🔹 Hotel Booking
- Browse hotels with photo galleries
- Book a hotel by number of persons, number of days, AC/non-AC room and food option
- **Automatic cost calculation** from daily rate, food charges and AC charges
- View booked hotel details

### 🔹 Destinations & Payment
- Destination gallery of popular tourist places
- **Easypaisa** payment option that opens the payment page

### 🔹 Admin Module
- Admin dashboard
- **Update** and **delete** customer records (deleting a customer also removes their bookings and account)
- **Create new tour packages** (ID, destination, date, cost)
- View customers, packages, hotels and destinations

---

## 🛠️ Tech Stack

### Frontend (Desktop GUI)
- Java Swing
- Java AWT (layouts, images, event handling)

### Backend
- Java (Object-Oriented Programming)
- JDBC (MySQL Connector/J)
- MySQL / MariaDB (via XAMPP)
- rs2xml (`net.proteanit.sql.DbUtils`) for displaying database results in tables

### Tools
- NetBeans IDE
- XAMPP and phpMyAdmin

---

## 🗄️ Database Design

Database: `tourism`

| Table | Purpose |
|---|---|
| `account` | User accounts with security question and answer |
| `customer` | Registered customer details |
| `package` | Tour packages created by the admin |
| `bookpackage` | Customer package bookings and total price |
| `hotels` | Hotels with daily, food and AC charges |
| `bookhotel` | Customer hotel bookings and total cost |

The file `tourism_schema.sql` contains the table structure and sample hotels and packages only. No personal data is included.

---

## 📸 Screenshots

> **Home – choose Admin or Customer**

![Home](screenshots/01-home-role-selection.jpg)

> **Login, Sign-up and Forgot Password**

![Login](screenshots/02-login.jpg)
![Sign up](screenshots/03-signup.jpg)
![Forgot password](screenshots/04-forgot-password.jpg)

> **Customer Dashboard and Registration**

![Customer dashboard](screenshots/05-customer-dashboard.jpg)
![Register customer](screenshots/06-register-customer.jpg)

> **Tour Packages and Package Booking**

![Tour packages](screenshots/07-tour-packages.jpg)
![Book package](screenshots/08-book-package.jpg)

> **Hotel Booking**

![Book hotel](screenshots/09-book-hotel.jpg)
![Booked hotel details](screenshots/10-view-booked-hotel.jpg)
![Hotels](screenshots/11-hotels.jpg)

> **Destinations and Payment**

![Destinations](screenshots/12-destinations.jpg)
![Easypaisa payment](screenshots/13-easypaisa-payment.jpg)

> **Admin Dashboard and Management**

![Admin dashboard](screenshots/14-admin-dashboard.jpg)
![Update customer](screenshots/15-update-customer.jpg)
![Delete customer](screenshots/16-delete-customer.jpg)
![Create package](screenshots/17-create-package.jpg)

> **Input Validation**

![Validation](screenshots/18-input-validation.jpg)

---

## ⚙️ How to Run

1. Install **JDK 8+**, **XAMPP** and **NetBeans** (or any Java IDE).
2. Start **MySQL** in XAMPP and create a database named `tourism`.
3. Import `tourism_schema.sql` using phpMyAdmin.
4. Add the **MySQL Connector/J** and **rs2xml** JAR files to the project libraries.
5. Check the connection settings in `Conn.java` (default: `localhost:3306`, user `root`, empty password).
6. Run `FrontPage.java`.

---

## 📊 Core Modules

- Front Page (role selection)
- Admin Login, Sign-up and Forgot Password
- Customer Login, Sign-up and Forgot Password
- Admin Dashboard
- Customer Dashboard
- Customer Registration
- Update Customer
- Delete Customer
- Create Package
- Check and Book Packages
- Check and Book Hotels
- Destinations
- Payment (Easypaisa)
- About

---

## 🔐 Security Review & Future Improvements

Looking back at this early project with a cyber security background, these are the improvements I would make:

- Use `PreparedStatement` for **every** query (some modules still build SQL with string concatenation, which can allow SQL injection)
- **Hash passwords** (e.g. bcrypt) instead of storing them in plain text
- Add **role-based access control** in the database instead of separate login screens only
- Move database credentials into a configuration file
- Add primary keys, foreign keys and numeric data types for prices and counts

---

## 🎯 Purpose of the Project

- Automate the daily work of a tourism company
- Keep customer, package and booking records in one central database
- Reduce manual paperwork and save time
- Provide a simple, user-friendly interface for both staff and customers

**Useful for:**
- Travel agencies and tour operators
- Hotel and package booking desks
- Learning Java Swing, JDBC and MySQL desktop development

---

Developed by **Noor Ullah Bacha**
Advanced Computer Programming project – Riphah International University (2021)
