```markdown
# 🛒 SpringBoot Shop Backend

A simple e-commerce backend built using **Spring Boot**, **Spring Data JPA**, and **H2 Database**.  
This application provides REST APIs for managing products, including image upload and retrieval.

---

## 📌 Project Overview

This project follows a standard layered architecture:

- **Controller Layer** – Handles HTTP requests
- **Service Layer** – Contains business logic
- **Repository Layer** – Handles database operations
- **Model Layer** – Defines the Product entity

Product images are stored directly in the database as `byte[]` using `@Lob`.

---

## 🏗️ Tech Stack

- Java  
- Spring Boot  
- Spring Web  
- Spring Data JPA  
- H2 In-Memory Database  
- Lombok  
- Maven  

---

## 🗃️ Product Entity Fields

- `id` (int)
- `name` (String)
- `description` (String)
- `brand` (String)
- `price` (BigDecimal)
- `category` (String)
- `releaseDate` (Date)
- `productAvailable` (boolean)
- `stockQuantity` (int)
- `imageName` (String)
- `imageType` (String)
- `imageData` (byte[])

---

## 🔌 API Endpoints

**Base URL**
```

[http://localhost:8080/api](http://localhost:8080/api)

```

### Get All Products
```

GET /products

```

### Get Product By ID
```

GET /product/{id}

```

### Add Product (With Image Upload)
```

POST /product
Content-Type: multipart/form-data

```

**Form Data Parameters**

| Key       | Type | Description                    |
|-----------|------|--------------------------------|
| product   | Text | JSON representation of product |
| imageFile | File | Product image file             |

### Get Product Image
```

GET /product/{productId}/image

````

Returns raw image bytes with the appropriate `Content-Type`.

---

## 🧪 Example Product JSON

```json
{
  "name": "iPhone 15",
  "description": "Latest Apple smartphone",
  "brand": "Apple",
  "price": 999.99,
  "category": "Electronics",
  "releaseDate": "2024-01-01",
  "productAvailable": true,
  "stockQuantity": 10
}
````

---


## 🛠️ How to Run

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/Raresssm/SpringBoot_Shop_Backend.git
cd SpringBoot_Shop_Backend
```

### 2️⃣ Build the Project

```bash
mvn clean install
```

### 3️⃣ Run the Application

```bash
mvn spring-boot:run
```

Application runs at:

```
http://localhost:8080
```

---

## 📌 Notes

* Uses H2 in-memory database (data resets on restart).
* Images are stored directly in the database.
* Lombok is used to reduce boilerplate code.

---

## 📄 License

This project is open-source. You may add a license file such as MIT if desired.

```
```
