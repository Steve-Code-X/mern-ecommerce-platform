# 04 - User Stories

# MERN Stack E-Commerce Application

## Introduction

User stories describe the features of the application from the perspective of the people who use it. They help the development team understand user needs and build features that provide real value.

Each user story follows this format:

> **As a *[user]*, I want to *[action]* so that *[benefit]*.**

Each story also includes **Acceptance Criteria**, which define when the feature is considered complete.

---

# Customer User Stories

## US-001: User Registration

**As a customer i want to create an account so that I can place orders and track my purchases.**

### Acceptance Criteria

* Customer can register with name, email, and password.
* Email must be unique.
* Password is securely encrypted.
* Registration is successful with valid data.

---

## US-002: User Login

**As a customer, I want to log in securely so that I can access my account.**

### Acceptance Criteria

* Customer can log in using email and password.
* Invalid credentials show an error.
* JWT token is generated after successful login.

---

## US-003: Browse Products

**As a customer, I want to browse available products so that I can find items to purchase.**

### Acceptance Criteria

* Product list loads successfully.
* Products display name, price, image, and category.
* Out-of-stock products are clearly indicated.

---

## US-004: Search Products

**As a customer, I want to search for products so that I can quickly find what I need.**

### Acceptance Criteria

* Search returns matching products.
* No results display a helpful message.

---

## US-005: View Product Details

**As a customer, I want to view detailed product information so that I can decide whether to buy it.**

### Acceptance Criteria

* Product page displays images, description, price, category, and stock status.

---

## US-006: Add Product to Cart

**As a customer, I want to add products to my cart so that I can purchase them later.**

### Acceptance Criteria

* Product can be added to the cart.
* Quantity can be updated.
* Cart total updates automatically.

---

## US-007: Checkout

**As a customer, I want to complete my purchase so that I can receive my products.**

### Acceptance Criteria

* Customer enters shipping information.
* Order is created successfully.
* Cart is cleared after checkout.

---

## US-008: View Order History

**As a customer, I want to view my previous orders so that I can track my purchases.**

### Acceptance Criteria

* Customer sees only their own orders.
* Order status is displayed.

---

# Administrator User Stories

## US-009: Admin Login

**As an administrator, I want to log in securely so that I can manage the store.**

### Acceptance Criteria

* Only admin users can access the admin dashboard.
* Unauthorized users are denied access.

---

## US-010: Manage Products

**As an administrator, I want to create, edit, and delete products so that I can keep the catalog up to date.**

### Acceptance Criteria

* Admin can add products.
* Admin can update product information.
* Admin can delete products.

---

## US-011: Manage Inventory

**As an administrator, I want to update product stock so that inventory remains accurate.**

### Acceptance Criteria

* Admin can increase or decrease stock.
* Stock cannot become negative.

---

## US-012: Manage Orders

**As an administrator, I want to view and update customer orders so that I can process them efficiently.**

### Acceptance Criteria

* Admin can view all orders.
* Admin can update order status (Pending, Processing, Shipped, Delivered).

---

# Future User Stories (Post-MVP)

These features are planned for future releases:

* Product Reviews
* Product Ratings
* Wishlist
* Coupons
* Live Chat
* Push Notifications
* Multi-language Support
* Loyalty Rewards

---

# Definition of Done

A user story is considered complete when:

* All acceptance criteria are met.
* Feature has been implemented.
* Code has been reviewed.
* Feature has been tested.
* Documentation has been updated.
* The issue has been marked as Done in GitHub Projects.
