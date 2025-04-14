# 🛒 Spring Boot E-Commerce Backend

## 📚 Overview

This project is a lightweight RESTful web service built with **Spring Boot**, designed to simulate the core backend functionalities of a basic e-commerce system. It supports managing **Users**, **Products**, **Carts**, and **Orders**, with clean separation between data models, services, repositories, and controllers.

---

## 🚀 Features

- Full CRUD operations for users, products, carts, and orders
- RESTful API design
- Data persistence using JSON files
- Layered architecture (Model–Repository–Service–Controller)
- Dependency Injection with Spring
- Docker containerization for easy deployment
- Unit tests for business logic

---

## 🛠 Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Scalable2025/Mini-Project1-Base.git
   cd Mini-Project1-Base
   ```

2. **Build the Project**
   ```bash
   mvn clean install
   ```

3. **Run the Application**
   ```bash
   mvn spring-boot:run
   ```

---

## 📂 Project Structure

```plaintext
src/
├── main/java/com/example/
│   ├── MiniProject1/              # Entry point
│   ├── data/                      # JSON data files
│   ├── model/                     # POJOs for User, Product, Cart, Order
│   ├── repository/                # Repositories for data access
│   ├── service/                   # Business logic
│   └── controller/                # REST API endpoints
└── test/java/com/example/         # Unit tests
```

---

## 🧩 Core Models

- **User**: Basic customer info and order history
- **Product**: Item data with name and price
- **Cart**: Temporary product storage for each user
- **Order**: Finalized list of purchased products with total price

Data is stored in JSON files located in the `data/` directory.

---

## 📡 REST API Overview

Example endpoints:

### 🔹 User
- `POST /user/` – Add a user  
- `GET /user/` – Get all users  
- `GET /user/{id}` – Retrieve user by ID  
- `POST /user/{id}/checkout` – Convert cart to order  
- `DELETE /user/delete/{id}` – Delete user  

### 🔹 Product
- `POST /product/` – Add a product  
- `GET /product/` – Get all products  
- `PUT /product/update/{id}` – Update product info  
- `PUT /product/applyDiscount` – Apply discount to products  
- `DELETE /product/delete/{id}` – Delete a product  

(Cart and Order endpoints are also included)

---

## 🧪 Testing

All services are covered by unit tests with meaningful test cases for each functionality.

To run tests:
```bash
mvn test
```

---

## 🐳 Docker Support

This project can be containerized easily using Docker.

- A `Dockerfile` is included.
- JSON data files should be mounted inside the container.
- Update environment variables accordingly.

---

## 📌 Notes

- Clean and extendable architecture
- Perfect starting point for a simple e-commerce API
- Can be enhanced with JWT authentication, database integration, or frontend support

---

Let me know if you'd like to add contributors, license info, or a live demo link.
