# Tourism-Management-System

A Java desktop application for managing a travel and tourism business — tour packages, hotel bookings, customers and payments — built with Java Swing, JDBC and MySQL.

# 🌍 Tourism Management System – Java Desktop Application

Tourism Management System helps a travel company manage its customers, tour packages, hotels and bookings from one place. Customers can register, browse tour packages and hotels, book them, see the total cost and pay, while the admin manages customers and creates new tour packages. All data is stored in a centralised MySQL database, replacing slow manual record-keeping with a fast, user-friendly system.


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

<img width="894" height="681" alt="01-home-role-selection" src="https://github.com/user-attachments/assets/477f2bc0-bd40-4668-9704-fe7aeb50f112" />


> **Login, Sign-up and Forgot Password**

<img width="688" height="397" alt="02-login" src="https://github.com/user-attachments/assets/211e6ee8-8a1a-41c1-94d5-21eec49c06be" />

<img width="692" height="408" alt="03-signup" src="https://github.com/user-attachments/assets/ae92d751-7b09-4380-9bd2-4467575e7a2a" />

<img width="838" height="395" alt="04-forgot-password" src="https://github.com/user-attachments/assets/f8972332-e42d-4d66-956f-b0dfcdb057c5" />


> **Customer Dashboard and Registration**

<img width="1920" height="962" alt="05-customer-dashboard" src="https://github.com/user-attachments/assets/6643c848-4eca-43e4-b137-1f3aa199e82a" />

<img width="839" height="546" alt="06-register-customer" src="https://github.com/user-attachments/assets/314d622c-84f2-49bf-8faa-5afa76fe08ec" />


> **Tour Packages and Package Booking**

<img width="915" height="623" alt="07-tour-packages" src="https://github.com/user-attachments/assets/4184b884-207d-4cf3-8b25-58782bfdb103" />

<img width="1106" height="459" alt="08-book-package" src="https://github.com/user-attachments/assets/6eeb573e-9878-440d-9884-0a579ed2272e" />


> **Hotel Booking**

<img width="1122" height="630" alt="09-book-hotel" src="https://github.com/user-attachments/assets/df74e020-5463-4808-8de4-3bd5953e6935" />

<img width="884" height="635" alt="10-view-booked-hotel" src="https://github.com/user-attachments/assets/fac1b253-b0cb-4025-a986-dace9b1c5da6" />

<img width="912" height="715" alt="11-hotels" src="https://github.com/user-attachments/assets/82e65227-36ab-4494-aa2f-d754e6b34d67" />


> **Destinations and Payment**

<img width="905" height="710" alt="12-destinations" src="https://github.com/user-attachments/assets/36a57e20-527a-41c2-a04e-4cfaad65a82f" />

<img width="808" height="812" alt="13-easypaisa-payment" src="https://github.com/user-attachments/assets/c0afeada-e911-4c9e-a33c-6abba26e0a46" />


> **Admin Dashboard and Management**

<img width="1916" height="974" alt="14-admin-dashboard" src="https://github.com/user-attachments/assets/87a0a005-92b8-41a3-b893-ebbef0883fca" />

<img width="840" height="550" alt="15-update-customer" src="https://github.com/user-attachments/assets/8808a3c4-04dc-47e2-80fe-33c4fc315494" />

<img width="854" height="560" alt="16-delete-customer" src="https://github.com/user-attachments/assets/07f1d14c-c180-4cc9-9d54-a2a6c0e05a05" />

<img width="557" height="451" alt="17-create-package" src="https://github.com/user-attachments/assets/c3ed99ee-8233-466f-963a-4b5409d57901" />


> **Input Validation**

<img width="713" height="418" alt="18-input-validation" src="https://github.com/user-attachments/assets/d4f9ce60-d074-4389-b684-9e489d842472" />


---

## ⚙️ How to Run

1. Install **JDK 8+**, **XAMPP** and **NetBeans** (or any Java IDE).
2. Start **MySQL** in XAMPP and create a database named `tourism`.
3. Import `tourism_schema.sql` using phpMyAdmin.
4. Add the **MySQL Connector/J** and **rs2xml** JAR files to the project libraries.
5. Check the connection settings in `Conn.java`.
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

# 📌 Source Code Availability & Disclaimer
This repository is shared for portfolio and educational showcase purposes only, highlighting the project's features and functionality through screenshots and descriptions.

The complete source code is not publicly available but may be provided upon request for professional or recruitment purposes, subject to applicable confidentiality restrictions.
