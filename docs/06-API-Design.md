# 07 - API Design Document

# MERN Stack E-Commerce Application

---

# 1. Purpose

The API Design Document defines all REST API endpoints used by the MERN Stack E-Commerce Application. It specifies how the frontend communicates with the backend, including request methods, URLs, authentication requirements, request bodies, and response formats.

---

# 2. API Standards

* Architecture: REST API
* Data Format: JSON
* Authentication: JWT (JSON Web Token)
* Base URL (Development): `http://localhost:5000/api`
* Base URL (Production): `https://your-backend-url/api`

---

# 3. Authentication API

## Register User

| Method | Endpoint       | Authentication |
| ------ | -------------- | -------------- |
| POST   | /auth/register | No             |

### Request Body

```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "password123"
}
```

### Success Response

```json
{
  "message": "User registered successfully",
  "user": {},
  "token": "jwt_token"
}
```

---

## Login User

| Method | Endpoint    | Authentication |
| ------ | ----------- | -------------- |
| POST   | /auth/login | No             |

### Request Body

```json
{
  "email": "john@example.com",
  "password": "password123"
}
```

### Success Response

```json
{
  "message": "Login successful",
  "token": "jwt_token"
}
```

---

# 4. Product API

## Get All Products

| Method | Endpoint  | Authentication |
| ------ | --------- | -------------- |
| GET    | /products | No             |

---

## Get Product By ID

| Method | Endpoint      | Authentication |
| ------ | ------------- | -------------- |
| GET    | /products/:id | No             |

---

## Create Product

| Method | Endpoint  | Authentication |
| ------ | --------- | -------------- |
| POST   | /products | Admin          |

---

## Update Product

| Method | Endpoint      | Authentication |
| ------ | ------------- | -------------- |
| PUT    | /products/:id | Admin          |

---

## Delete Product

| Method | Endpoint      | Authentication |
| ------ | ------------- | -------------- |
| DELETE | /products/:id | Admin          |

---

# 5. Category API

## Get Categories

| Method | Endpoint    | Authentication |
| ------ | ----------- | -------------- |
| GET    | /categories | No             |

---

## Create Category

| Method | Endpoint    | Authentication |
| ------ | ----------- | -------------- |
| POST   | /categories | Admin          |

---

# 6. Cart API

## Get Cart

| Method | Endpoint | Authentication |
| ------ | -------- | -------------- |
| GET    | /cart    | Customer       |

---

## Add Item to Cart

| Method | Endpoint | Authentication |
| ------ | -------- | -------------- |
| POST   | /cart    | Customer       |

---

## Update Cart Item

| Method | Endpoint  | Authentication |
| ------ | --------- | -------------- |
| PUT    | /cart/:id | Customer       |

---

## Remove Cart Item

| Method | Endpoint  | Authentication |
| ------ | --------- | -------------- |
| DELETE | /cart/:id | Customer       |

---

# 7. Order API

## Create Order

| Method | Endpoint | Authentication |
| ------ | -------- | -------------- |
| POST   | /orders  | Customer       |

---

## Get My Orders

| Method | Endpoint   | Authentication |
| ------ | ---------- | -------------- |
| GET    | /orders/my | Customer       |

---

## Get All Orders

| Method | Endpoint | Authentication |
| ------ | -------- | -------------- |
| GET    | /orders  | Admin          |

---

## Update Order Status

| Method | Endpoint    | Authentication |
| ------ | ----------- | -------------- |
| PUT    | /orders/:id | Admin          |

---

# 8. HTTP Status Codes

| Code | Meaning               |
| ---- | --------------------- |
| 200  | OK                    |
| 201  | Created               |
| 400  | Bad Request           |
| 401  | Unauthorized          |
| 403  | Forbidden             |
| 404  | Not Found             |
| 500  | Internal Server Error |

---

# 9. Error Response Format

```json
{
  "success": false,
  "message": "Error description"
}
```

---

# 10. Success Response Format

```json
{
  "success": true,
  "message": "Request completed successfully",
  "data": {}
}
```

---

# 11. Authentication Flow

1. User registers or logs in.
2. Backend validates credentials.
3. Backend generates a JWT.
4. Frontend stores the JWT.
5. JWT is sent in the Authorization header for protected requests.
6. Backend verifies the JWT before granting access.

---

# 12. API Summary

The API follows REST principles and provides secure endpoints for authentication, product management, shopping cart operations, category management, and order processing. Protected endpoints require JWT authentication, and administrator-only endpoints enforce role-based authorization.
