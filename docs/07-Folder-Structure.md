# 08 - Folder Structure Document

# MERN Stack E-Commerce Application

---

# 1. Purpose

The Folder Structure Document defines how the project files and directories are organized. A consistent folder structure improves code readability, maintainability, collaboration, and scalability.

---

# 2. Project Structure

```text
mern-ecommerce/
│
├── client/                 # React Frontend
├── server/                 # Node.js Backend
├── docs/                   # Project Documentation
├── README.md
├── .gitignore
└── LICENSE
```

---

# 3. Frontend Folder Structure

```text
client/
│
├── public/
│
├── src/
│   ├── assets/
│   ├── components/
│   ├── layouts/
│   ├── pages/
│   ├── routes/
│   ├── services/
│   ├── hooks/
│   ├── context/
│   ├── utils/
│   ├── styles/
│   ├── App.jsx
│   └── main.jsx
│
├── package.json
└── vite.config.js
```

### Folder Responsibilities

* **assets/** – Images, icons, fonts
* **components/** – Reusable UI components
* **layouts/** – Shared page layouts
* **pages/** – Application pages
* **routes/** – Route definitions
* **services/** – API communication (Axios)
* **hooks/** – Custom React hooks
* **context/** – Global state management
* **utils/** – Helper functions
* **styles/** – Global CSS and styling

---

# 4. Backend Folder Structure

```text
server/
│
├── src/
│   ├── config/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── services/
│   ├── validators/
│   ├── utils/
│   ├── app.js
│   └── server.js
│
├── package.json
└── .env
```

### Folder Responsibilities

* **config/** – Database and application configuration
* **controllers/** – Handle HTTP requests and responses
* **middleware/** – Authentication and custom middleware
* **models/** – Mongoose schemas and models
* **routes/** – Express route definitions
* **services/** – Business logic
* **validators/** – Input validation
* **utils/** – Utility functions
* **app.js** – Express application setup
* **server.js** – Server entry point

---

# 5. Documentation Folder

```text
docs/
│
├── 01-project-overview.md
├── 02-business-requirements.md
├── 03-functional-requirements.md
├── 04-user-stories.md
├── 05-system-design.md
├── 06-database-design.md
├── 07-api-design.md
├── 08-folder-structure.md
├── 09-development-roadmap.md
└── 10-deployment-plan.md
```

---

# 6. Naming Conventions

* Use **camelCase** for variables and functions.
* Use **PascalCase** for React components.
* Use **kebab-case** for folder names where appropriate.
* Use clear, descriptive file names.

Examples:

* ProductCard.jsx
* authController.js
* orderService.js
* userRoutes.js

---

# 7. Architecture Principles

The project follows these principles:

* Separation of Concerns
* Reusability
* Maintainability
* Scalability
* Modular Design

Each folder has a single responsibility, making the application easier to develop and maintain.

---

# 8. Summary

The folder structure provides a clean and organized foundation for the MERN Stack E-Commerce Application. By separating frontend, backend, and documentation, the project becomes easier to understand, extend, and collaborate on as it grows.
