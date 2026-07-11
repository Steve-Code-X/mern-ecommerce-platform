# 06 - Database Design Document

# MERN Stack E-Commerce Application

---

# 1. Purpose

The Database Design Document defines how application data will be stored, organized, and related within MongoDB. It serves as the blueprint for creating Mongoose models and ensures that data is structured consistently before development begins.

---

# 2. Database Technology

* **Database:** MongoDB Atlas
* **ODM:** Mongoose
* **Database Type:** NoSQL (Document Database)

---

# 3. Collections

The application will use the following collections:

* Users
* Products
* Categories
* Orders

---

# 4. User Collection

### Description

Stores customer and administrator account information.

### Fields

| Field     | Type     | Required | Description           |
| --------- | -------- | -------- | --------------------- |
| _id       | ObjectId | Yes      | Unique identifier     |
| name      | String   | Yes      | User's full name      |
| email     | String   | Yes      | Unique email address  |
| password  | String   | Yes      | Encrypted password    |
| role      | String   | Yes      | customer or admin     |
| createdAt | Date     | Yes      | Account creation date |
| updatedAt | Date     | Yes      | Last updated date     |

---

# 5. Category Collection

### Description

Stores product categories.

### Fields

| Field       | Type     | Required | Description          |
| ----------- | -------- | -------- | -------------------- |
| _id         | ObjectId | Yes      | Unique identifier    |
| name        | String   | Yes      | Category name        |
| description | String   | No       | Category description |
| createdAt   | Date     | Yes      | Creation date        |
| updatedAt   | Date     | Yes      | Last updated date    |

---

# 6. Product Collection

### Description

Stores product information.

### Fields

| Field       | Type     | Required | Description           |
| ----------- | -------- | -------- | --------------------- |
| _id         | ObjectId | Yes      | Unique identifier     |
| name        | String   | Yes      | Product name          |
| description | String   | Yes      | Product description   |
| price       | Number   | Yes      | Product price         |
| stock       | Number   | Yes      | Available quantity    |
| image       | String   | No       | Product image URL     |
| category    | ObjectId | Yes      | Reference to Category |
| createdAt   | Date     | Yes      | Creation date         |
| updatedAt   | Date     | Yes      | Last updated date     |

---

# 7. Order Collection

### Description

Stores customer orders.

### Fields

| Field           | Type     | Required | Description                             |
| --------------- | -------- | -------- | --------------------------------------- |
| _id             | ObjectId | Yes      | Unique identifier                       |
| user            | ObjectId | Yes      | Reference to User                       |
| items           | Array    | Yes      | Purchased products                      |
| totalAmount     | Number   | Yes      | Total order value                       |
| status          | String   | Yes      | Pending, Processing, Shipped, Delivered |
| shippingAddress | Object   | Yes      | Delivery details                        |
| createdAt       | Date     | Yes      | Order creation date                     |
| updatedAt       | Date     | Yes      | Last updated date                       |

---

# 8. Relationships

The collections are related as follows:

* One Category can contain many Products.
* One User can place many Orders.
* One Order belongs to one User.
* One Order contains one or more Products.

---

# 9. Data Validation Rules

The application will enforce the following rules:

* Email addresses must be unique.
* Passwords are stored as hashed values.
* Product prices cannot be negative.
* Product stock cannot be negative.
* Every product must belong to a category.
* Every order must belong to a registered user.

---

# 10. Indexing Strategy

To improve query performance, indexes will be created on:

* email (User)
* name (Product)
* category (Product)
* status (Order)

---

# 11. Future Database Enhancements

Future versions may include additional collections:

* Reviews
* Wishlist
* Coupons
* Payments
* Notifications
* Shipping

These collections are outside the scope of Version 1 (MVP).

---

# 12. Database Design Summary

The database is designed to support a secure and scalable e-commerce application. Collections are organized to reduce duplication, maintain relationships between entities, and provide a solid foundation for future feature expansion.


