first we initialise our project and put all dependencies in cargo.toml

# 📦 **Dependency Breakdown**

## 🔐 **Security & Auth**

### **argon2**

* Library for hashing passwords using the Argon2 algorithm (best practice for secure password storage).

### **jsonwebtoken**

* Used to generate and verify JWT tokens (for login, access tokens, refresh tokens, etc.).

### **validator**

* Provides validation macros (e.g., `#[validate(email)]`) for request DTOs.

---

# 🧵 **Async & Utilities**

### **async-trait**

* Lets you write async functions inside traits (Rust normally doesn’t support this).

### **tokio**

* The async runtime (executor, task scheduler, timers, TCP, etc.) that Axum runs on.

---

# ⏳ **Time & Dates**

### **chrono**

* Handles date/time types (`DateTime`, `Utc`, etc.), with serialization via serde.

---

# 🔧 **Environment**

### **dotenvy**

* Loads environment variables from a `.env` file (e.g., DB connection string, JWT secret).

---

# 📦 **Serialization**

### **serde / serde_json**

* `serde` → Serialize/deserialize Rust structs.
* `serde_json` → Convert to/from JSON strings (common for API responses).

---

# 🗄️ **Database**

### **sqlx**

* Async, compile-time-checked SQL query library (supports query macros).
* Features enabled:

  * **postgres** → PostgreSQL backend.
  * **chrono** → Support for `DateTime`.
  * **uuid** → Maps SQL UUID to Rust `uuid`.
  * **runtime-async-std-native-tls** → TLS + runtime support.

### **uuid**

* Generates UUIDs (`v4`) for user IDs, sessions, and supports serialization.

---

# 🌐 **Web Framework**

### **axum**

* Your HTTP framework (routes, middleware, handlers). Fast, async, built on Tower.

### **axum-extra**

* Adds extra features like **cookie extraction**, helpful for storing JWTs in cookies.

---

# 🏗️ **Tower Ecosystem**

### **tower**

* Provides middleware building blocks used internally by Axum.

### **tower-http**

* HTTP-related middleware:

  * **cors** → CORS support.
  * **trace** → Request tracing/logging.

---

# 📊 **Logging**

### **tracing-subscriber**

* Handles structured logging (filters, layers, formatting) for the `tracing` crate.

---

# ✉️ **Email**

### **lettre**

* Send emails (SMTP or providers).
* Useful for **email verification**, **password reset**, etc.

---

# ✅ Summary Table

| Dependency         | Purpose                         |
| ------------------ | ------------------------------- |
| argon2             | Password hashing                |
| async-trait        | Async support in traits         |
| chrono             | Time/date handling              |
| dotenvy            | Load .env environment variables |
| jsonwebtoken       | Create/verify JWTs              |
| serde              | Serialization framework         |
| serde_json         | JSON encoding/decoding          |
| sqlx               | Async Postgres database ORM-ish |
| uuid               | UUID support                    |
| validator          | Input validations               |
| axum               | Web framework                   |
| axum-extra         | Cookies & extra extractors      |
| tokio              | Async runtime for Axum          |
| tower              | Middleware foundation           |
| tower-http         | HTTP middleware (CORS, tracing) |
| tracing-subscriber | Logging system                  |
| lettre             | Sending emails                  |

