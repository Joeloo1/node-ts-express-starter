# Node.js + TypeScript + Express Starter

A modern, production-ready boilerplate for building scalable and secure REST APIs using Express 5 and TypeScript 6.

## 🚀 Features

- **Standard Tech Stack**: Node.js, Express 5, and TypeScript 6.
- **Security Hardened**: Pre-configured with `helmet` for security headers and `express-rate-limit` to prevent brute force attacks.
- **Graceful Shutdown**: Properly handles `SIGTERM` and `SIGINT` signals for clean exits in containerized environments.
- **Advanced Logging**: Centralized logging using `winston` (with file rotation support) and HTTP request logging via `morgan`.
- **Path Aliases**: Clean imports using `@/` aliases (e.g., `@/services/...` instead of `../../../services/...`).
- **Code Quality**: Pre-configured ESLint 10 and Prettier for consistent code style.
- **Error Handling**: Standardized `AppError` class and centralized global error middleware.
- **Environment Management**: Type-safe environment variable configuration using `dotenv`.

---

## 📂 Project Structure

```text
src/
├── config/       # Environment variables and logger configuration
├── controller/   # Request handlers (logic for routes)
├── middleware/   # Express middlewares (auth, error handling, etc.)
├── routes/       # API route definitions
├── services/     # Business logic layer
├── utils/        # Utility classes and helper functions
├── app.ts        # Express app initialization
└── server.ts     # Server entry point and graceful shutdown logic
```

---

## 🛠️ Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v20+ recommended)
- [pnpm](https://pnpm.io/) (v10+ recommended)

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd node-ts-express-starter
   ```

2. Install dependencies:
   ```bash
   pnpm install
   ```

3. Configure environment variables:
   Create a `.env` file in the root directory and add your variables:
   ```env
   PORT=3000
   NODE_ENV=development
   ```

### Development

Run the server in development mode with hot-reloading:
```bash
pnpm dev
```

### Production

1. Build the project:
   ```bash
   pnpm build
   ```

2. Start the production server:
   ```bash
   pnpm start
   ```

---

## 🧹 Code Quality

- **Linting**: `pnpm lint` or `pnpm lint:fix`
- **Formatting**: `pnpm format`

---

## 🛡️ License

This project is licensed under the [ISC License](LICENSE).
