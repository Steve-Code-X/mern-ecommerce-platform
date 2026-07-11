# 02 - Business Requirements Document (BRD)

# MERN Stack E-Commerce Application

## 1. Business Background

The MERN Stack E-Commerce Application is a web-based online shopping platform designed for small and medium-sized businesses. It allows customers to browse products, add items to a shopping cart, place orders, and manage their accounts. The system also provides administrators with tools to manage products, inventory, customers, and orders through a secure admin dashboard.

The goal of this project is to provide a modern, scalable, and user-friendly online shopping experience while simplifying business operations.

---

# 2. Business Problem

Many small businesses rely only on physical stores or outdated systems to sell their products. This creates several problems:

* Customers cannot shop online.
* Business owners manually manage inventory.
* Orders are tracked manually.
* Customers have limited shopping hours.
* Businesses lose potential online sales.
* Managing products becomes difficult as the business grows.

The business needs an online platform that automates these processes and improves the customer experience.

---

# 3. Business Objectives

The project aims to achieve the following business goals:

* Provide a modern online shopping platform.
* Allow customers to purchase products from anywhere.
* Increase business sales through online ordering.
* Improve customer satisfaction with an easy shopping experience.
* Reduce manual work involved in product and order management.
* Enable administrators to manage products, inventory, and orders efficiently.
* Build a scalable system that can support future growth.

---

# 4. Stakeholders

| Stakeholder             | Responsibility                                             |
| ----------------------- | ---------------------------------------------------------- |
| Business Owner          | Defines business goals and requirements                    |
| Customers               | Browse products and place orders                           |
| Administrator           | Manages products, inventory, and customer orders           |
| Developers              | Design, develop, test, and maintain the application        |
| Future Maintenance Team | Monitor, maintain, and improve the system after deployment |

---

# 5. Business Rules

The following business rules apply to the application:

* Customers must register before placing an order.
* Customers must log in to view their order history.
* Only administrators can create, update, or delete products.
* Products cannot have negative stock quantities.
* Every order belongs to one registered customer.
* Passwords must be securely encrypted before storage.
* Each product must belong to a valid category.
* Customers can only manage their own orders.
* Administrators can manage all products and orders.

---

# 6. Assumptions

The following assumptions are made during project planning:

* Users have access to the internet.
* Customers have valid email addresses.
* MongoDB Atlas will be available for database hosting.
* The application will use JWT for authentication.
* The application will be deployed online using Vercel and Render (or Railway).
* The initial version will focus on the Minimum Viable Product (MVP).

---

# 7. Constraints

The project has the following constraints:

* Frontend must be developed using React.
* Backend must be developed using Node.js and Express.js.
* MongoDB will be used as the primary database.
* Authentication will use JWT and bcrypt.
* Development will follow the GitHub workflow.
* The project will be completed in phases.
* Advanced features will be postponed until after the MVP.

---

# 8. Business Scope

## Included in Version 1 (MVP)

### Customer Features

* User Registration
* User Login
* Product Browsing
* Product Search
* Product Details
* Shopping Cart
* Checkout
* Order History
* User Profile

### Administrator Features

* Admin Login
* Dashboard
* Product Management (Create, Read, Update, Delete)
* Inventory Management
* Order Management

---

## Excluded from Version 1

The following features will be considered for future releases:

* Product Reviews
* Product Ratings
* Wishlist
* Coupons and Discount
* Multi-language Support
* Multi-vendor Marketplace
* Loyalty Rewards
* Push Notifications

---

# 9. Success Criteria

The project will be considered successful when:

* Customers can register and log in securely.
* Customers can browse products and place orders.
* Administrators can manage products and orders.
* Product inventory is updated correctly.
* The application is responsive on desktop and mobile devices.
* The application is successfully deployed online.
* The codebase is organized, documented, and maintained using GitHub best practices.

---

# 10. Approval

This document defines the business requirements for Version 1 (MVP) of the MERN Stack E-Commerce Application. It serves as the foundation for functional requirements, system design, database design, API planning, development, testing, and deployment.
