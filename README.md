# 🚀 express-ts-starter

A feature-rich Express.js boilerplate with TypeScript support, scalable folder structure, custom import aliases, CLI-based module generation, and built-in linting + formatting support. Perfect for starting REST APIs fast with maintainability in mind.

---

## ✨ Features

- ✅ TypeScript Support
- ✅ Clean & Scalable Folder Structure
- ✅ Module-Based CLI Generator
- ✅ Custom Import Aliases (`@/controller`, `@/service`, etc.)
- ✅ ESLint + Prettier + Husky for Clean Code & Pre-commit
- ✅ Centralized Error & Validation Middleware
- ✅ Configurable Environment & Logging
- ✅ Mongoose or Sequelize Ready

---

### How to use CLI

```bash
npm run cli
```

or

```bash
make cli
```

- It will ask you module name
- Based on that will create controller, route and validation files inside API folder

## 📁 Recommended Folder Structure:

```bash

project-root/
│
├── src/
│ ├── api/                                     # Group controllers, routes, and validation by feature
│ │ ├── user/
│ │ │ ├── user.controller.ts             # User controller
│ │ │ ├── user.route.ts                   # User routes
│ │ │ ├── user.validation.ts            # User input validation (optional)
│ │ │ └── user.service.ts                # User-specific services
│ │ ├── auth/
│ │ │ ├── auth.controller.ts             # auth controller
│ │ │ ├── auth.route.ts                   # auth routes
│ │ │ ├── auth.validation.ts            # auth input validation (optional)
│ │ │ └── auth.service.ts                # auth-specific services
│ ├──  database/
│ │ ├──  Redis.database.js
│ │ ├── Mongo.database.js
│ │ └── auth/
│ │ ├── auth.controller.ts               # Auth controller
│ │ ├── auth.route.ts                     # Auth routes
│ │ ├── auth.service.ts                   # Auth service
│ │ └── auth.validation.ts               # Auth validation (optional)
│ │
│ ├── config/                                 # App configuration (environment, database, etc.)
│ │ ├── database.ts                        # Database connection
│ │ ├── env.ts                                # Environment variable configuration
│ │ └── logger.ts                            # Logger configuration
│ │
│ ├── middlewares/                         # Custom middleware (authentication, error handling)
│ │ ├── error.middleware.ts              # Centralized error handling
│ │ ├── auth.middleware.ts              # Auth middleware for protected routes
│ │ └── validate.middleware.ts          # Validation middleware for request schemas
│ │
│ ├── models/                                   # Mongoose/Sequelize models or DB schemas
│ │ ├── user.model.ts                         # User model (Mongoose, Sequelize, etc.)
│ │ └── auth.model.ts                         # Auth-related model (tokens, sessions, etc.)
│ │
│ ├── services/                                  # Business logic and reusable services
│ │ ├── email.service.t                        # Email service (send emails)
│ │ ├── auth.service.ts                        # Authentication and authorization service
│ │ └── user.service.ts                         # User-related services (CRUD operations)
│ │
│ ├── utils/                                        # Helper functions/utilities (non-business logic)
│ │ ├── httpResponse.ts                       # Standardized response format
│ │ ├── constants.ts                            # App constants
│ │ └── hash.ts                                   # Password hashing utility
│ │
│ ├── validations/                               # Centralized validation schemas (using Zod, Joi, etc.)
│ │ ├── user.validation.ts                     # User-related validation
│ │ └── auth.validation.ts                    # Auth validation
│ │
│ ├── app.ts                                        # Initialize Express app
│ └── index.ts                                      # Main entry point to start the server
│
├── dist/                                             # Compiled JavaScript files (from TypeScript)
│
├── node_modules/                              # Dependencies
│
├── .env                                              # Environment variables
├── .eslintignore                                  # ESLint ignore patterns
├── .eslintrc.json                                  # ESLint configuration
├── .gitignore                                      # Ignore node_modules and dist
├── package.json                                 # Project dependencies and scripts
├── tsconfig.json                                 # TypeScript configuration
└── README.md


```

# ✅ Scripts

Script Description
npm start Start compiled server
npm run dev Start server in dev mode using ts-node-dev
npm run build Build TypeScript files to /dist
npm run lint Run ESLint
npm run cli Run custom CLI for generating modules

# ⚙️ Technologies Used

- Express.js

- TypeScript

- ESLint + Prettier

- Husky (pre-commit lint)

- Zod / Joi (for validation – configurable)

- Mongoose or Sequelize (based on setup)

# 🧪 Future Improvements

✅ Docker support

✅ Swagger documentation integration

✅ Testing (Jest + Supertest)

✅ Authentication examples (JWT, Sessions)

📄 License
MIT License — free to use, modify, and distribute.

🙌 Contributing
PRs are welcome. Please lint before pushing:

```bash
npm run lint
```

💡 Inspiration
Built for backend developers who want a clean, scalable, and maintainable starter for Express + TypeScript.
