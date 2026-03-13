# PawShop — Pet Management & Shopping Platform

> **CSE370: Database Management** — BRAC University  
> **Author:** Mazbha Ul Haque (ID: 22101514)

---

## Overview

**PawShop** is a full-stack web application that serves as a one-stop platform for pet owners to manage their pets and purchase pet products online. Built as a course project for CSE370 (Database Management), the application demonstrates core database design principles including ER modeling, normalization, complex SQL queries, and relational schema implementation using MySQL.

---

## Features

- **User Registration & Authentication** — Secure signup and login system with session management
- **Pet Profile Management** — Add, edit, and manage profiles for your pets (name, breed, age, medical info)
- **Product Catalog** — Browse a wide range of pet products including food, accessories, toys, and grooming supplies
- **Shopping Cart & Checkout** — Add items to cart and complete purchases seamlessly
- **Order History & Tracking** — View past orders and track current order status
- **Responsive UI** — Clean, modern interface built with React and Vite

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| **Frontend** | React.js, Vite, HTML, CSS |
| **Backend** | Node.js, Express.js |
| **Database** | MySQL |
| **API** | RESTful API architecture |

---

## Project Structure

```
PawShop/
├── Backend/
│   ├── routes/              # API route handlers
│   ├── connect.js           # MySQL database connection config
│   ├── index.js             # Express server entry point
│   ├── package.json
│   └── package-lock.json
│
├── Frontend/
│   ├── public/              # Static assets
│   ├── Registration/        # Registration page components
│   ├── src/                 # React source code (components, pages, styles)
│   ├── index.html           # App entry point
│   ├── vite.config.js       # Vite configuration
│   ├── .eslintrc.cjs        # ESLint config
│   ├── .gitignore
│   ├── package.json
│   └── package-lock.json
│
└── README.md
```

---

## Database Design

The project implements a normalized relational database schema in MySQL with the following key entities:

- **Users** — Stores user credentials and profile information
- **Pets** — Pet details linked to their owners (one-to-many relationship)
- **Products** — Product catalog with categories, pricing, and stock info
- **Orders** — Purchase records with timestamps and status tracking
- **Order_Items** — Junction table linking orders to products (many-to-many)
- **Cart** — Temporary shopping cart items per user

---

## How to Run

### Prerequisites
- Node.js (v16+)
- MySQL Server
- npm

### 1. Clone the repository
```bash
git clone https://github.com/mazbha-37/CSE370_Project.git
cd CSE370_Project
```

### 2. Setup the database
- Create a MySQL database (e.g., `pawshop_db`)
- Import the provided SQL schema file to create the tables

### 3. Configure backend
```bash
cd Backend
npm install
```
Update `connect.js` with your MySQL credentials:
```javascript
const connection = mysql.createConnection({
  host: "localhost",
  user: "your_username",
  password: "your_password",
  database: "pawshop_db"
});
```

### 4. Start the backend server
```bash
node index.js
```

### 5. Setup and start the frontend
```bash
cd ../Frontend
npm install
npm run dev
```

The app will be running at `http://localhost:5173`

---

## Course Information

| | |
|---|---|
| **Course** | CSE370: Database Management |
| **University** | BRAC University |
| **Student** | Mazbha Ul Haque |
| **Student ID** | 22101514 |

---

## License

This project is developed for academic purposes as part of the CSE370 coursework at BRAC University.
