# 🛒 Phimart - E-commerce REST API with Django DRF

**Phimart** is a scalable and modular e-commerce backend API built using **Django** and **Django REST Framework**. It supports full user authentication, product and category management, shopping cart functionality, and order processing. Designed with RESTful principles, token-based authentication, and interactive API documentation, it’s suitable for real-world use cases and learning advanced backend development.

---

## 🚀 Overview

Phimart enables the following capabilities:

- Users can register, log in, and authenticate using JWT tokens.
- Admins can manage products and categories.
- Customers can add/remove products from their cart.
- Users can place and manage orders.
- All APIs are documented using Swagger and ReDoc interfaces.

---

## ✨ Core Features

| Category                  | Description                                                                     |
| ------------------------- | ------------------------------------------------------------------------------- |
| 🧾 **Product Management** | CRUD operations for products and product categories                             |
| 🛒 **Cart System**        | Add, view, and remove items from the user’s cart                                |
| 📦 **Order Management**   | Place orders, view order history, and manage order states                       |
| 🔐 **Authentication**     | JWT-based authentication using **Djoser** and **SimpleJWT**                     |
| 📚 **API Documentation**  | Interactive API docs via **Swagger UI** and **ReDoc** (powered by **drf-yasg**) |

---

## 🧰 Tech Stack

| Technology                      | Purpose                              |
| ------------------------------- | ------------------------------------ |
| **Django**                      | Core web framework                   |
| **Django REST Framework (DRF)** | REST API development                 |
| **Djoser**                      | User authentication and management   |
| **SimpleJWT**                   | JSON Web Token (JWT) authentication  |
| **drf-yasg**                    | Swagger and ReDoc documentation      |
| **PostgreSQL**                  | Primary database (production-ready)  |
| **SQLite**                      | Lightweight default DB for local use |
| **dotenv**                      | Environment variable management      |

---

## 🛠️ Installation & Setup

> Make sure you have **Python 3.8+**, **pip**, and optionally **PostgreSQL** installed.

### 🔁 1. Clone the repository

```bash
git clone https://github.com/algoabrar/phimart.git
cd phimart
```

### 🧪 2. Create & activate a virtual environment

```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

### 📦 3. Install the dependencies

```bash
pip install -r requirements.txt
```

### 🧱 4. Apply database migrations

```bash
python manage.py migrate
```

### 👤 5. Create a superuser (admin access)

```bash
python manage.py createsuperuser
```

### 🚀 6. Start the development server

```bash
python manage.py runserver
```

Visit:
📍 [http://127.0.0.1:8000/](http://127.0.0.1:8000/)

---

## 🧾 API Documentation

| Tool    | URL                                                              |
| ------- | ---------------------------------------------------------------- |
| Swagger | [http://127.0.0.1:8000/swagger/](http://127.0.0.1:8000/swagger/) |

---

## 🔐 Authentication

Phimart uses **JWT** authentication via Djoser and SimpleJWT.

### Common Endpoints:

| Method | Endpoint             | Description                    |
| ------ | -------------------- | ------------------------------ |
| POST   | `/auth/users/`       | Register a new user            |
| POST   | `/auth/jwt/create/`  | Obtain access & refresh tokens |
| POST   | `/auth/jwt/refresh/` | Refresh access token           |
| POST   | `/auth/jwt/verify/`  | Verify token validity          |

> All protected endpoints require the `Authorization: Bearer <your_token>` header.

---

## 🔧 Environment Variables

Create a `.env` file in the project root:

```ini
SECRET_KEY=your_django_secret_key
DEBUG=True
DATABASE_URL=your_database_url  # e.g., postgres://user:password@localhost:5432/phimart
ALLOWED_HOSTS=127.0.0.1,localhost
EMAIL_HOST=smtp.example.com
EMAIL_PORT=587
EMAIL_HOST_USER=your_email@example.com
EMAIL_HOST_PASSWORD=your_email_password
EMAIL_USE_TLS=True
```

> Use `python-decouple` for better environment variable management (optional).

---

## ✅ Future Enhancements

- ✅ Pagination and filtering
- ✅ Custom permissions (admin, staff, customer roles)
- ⏳ Payment gateway integration (Stripe/PayPal)
- ⏳ Product reviews & ratings
- ⏳ Multi-vendor support
- ⏳ Docker & production deployment setup

---

## 📜 License

This project is licensed under the **MIT License**.
See the [LICENSE](LICENSE) file for full details.

---

## 👤 Author

Made with ❤️ by **[Saiyedul Abrar](https://github.com/algoabrar)**
For collaboration, suggestions, or feedback, feel free to connect via GitHub.
