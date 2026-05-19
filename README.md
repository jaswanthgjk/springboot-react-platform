# 🛒 Full Stack Product Management Platform

A production-grade full stack application built with **Java Spring Boot** and **React.js**, demonstrating enterprise-level architecture patterns including REST APIs, JWT authentication, PostgreSQL persistence, and Docker containerization.

---

## 🚀 Live Demo

> Deploy to AWS / Render / Railway and add link here

---

## 🛠 Tech Stack

**Backend**
- Java 17 + Spring Boot 3.x
- Spring Security + JWT Authentication
- Hibernate / JPA + PostgreSQL
- REST APIs with proper error handling
- Maven build system

**Frontend**
- React.js 18 + TypeScript
- Redux Toolkit for state management
- Axios for API calls
- CSS Modules for styling

**DevOps**
- Docker + Docker Compose
- GitHub Actions CI/CD pipeline
- Environment-based configuration

---

## 📁 Project Structure

```
├── backend/
│   ├── src/main/java/com/jaswanth/
│   │   ├── controller/        # REST Controllers
│   │   ├── service/           # Business Logic
│   │   ├── repository/        # JPA Repositories
│   │   ├── model/             # Entity Classes
│   │   ├── dto/               # Data Transfer Objects
│   │   ├── security/          # JWT + Spring Security
│   │   └── config/            # App Configuration
│   └── pom.xml
├── frontend/
│   ├── src/
│   │   ├── components/        # React Components
│   │   ├── pages/             # Page Components
│   │   ├── store/             # Redux Store
│   │   ├── services/          # API Services
│   │   └── types/             # TypeScript Types
│   └── package.json
├── docker-compose.yml
└── README.md
```

---

## ⚙️ How to Run Locally

### Prerequisites
- Java 17+
- Node.js 18+
- Docker Desktop
- PostgreSQL (or use Docker)

### With Docker (Recommended)
```bash
# Clone the repo
git clone https://github.com/jaswanthgjk/springboot-react-platform.git
cd springboot-react-platform

# Start everything
docker-compose up --build

# App runs at:
# Frontend: http://localhost:3000
# Backend:  http://localhost:8080
# Postgres: localhost:5432
```

### Manual Setup
```bash
# Backend
cd backend
./mvnw spring-boot:run

# Frontend (new terminal)
cd frontend
npm install
npm start
```

---

## 🔑 Key Features

- ✅ JWT-based authentication and authorization
- ✅ Full CRUD operations with validation
- ✅ Role-based access control (Admin / User)
- ✅ Pagination and sorting on all list endpoints
- ✅ Global error handling with proper HTTP status codes
- ✅ CORS configuration for frontend-backend communication
- ✅ Dockerized for consistent environments
- ✅ CI/CD with GitHub Actions

---

## 📡 API Endpoints

| Method | Endpoint | Description | Auth |
|--------|----------|-------------|------|
| POST | `/api/auth/login` | User login | ❌ |
| POST | `/api/auth/register` | User registration | ❌ |
| GET | `/api/products` | Get all products | ✅ |
| GET | `/api/products/{id}` | Get product by ID | ✅ |
| POST | `/api/products` | Create product | ✅ Admin |
| PUT | `/api/products/{id}` | Update product | ✅ Admin |
| DELETE | `/api/products/{id}` | Delete product | ✅ Admin |

---

## 🧪 Running Tests

```bash
# Backend tests
cd backend
./mvnw test

# Frontend tests
cd frontend
npm test
```

---

## 📊 Architecture Diagram

```
┌─────────────┐     HTTP/REST      ┌──────────────────┐
│  React.js   │ ◄────────────────► │  Spring Boot API  │
│  Frontend   │                    │   (Port 8080)     │
└─────────────┘                    └────────┬─────────┘
                                            │ JPA/Hibernate
                                   ┌────────▼─────────┐
                                   │   PostgreSQL DB   │
                                   │   (Port 5432)     │
                                   └──────────────────┘
```

---

## 👨‍💻 Author

**Jaswanth Kumar Ganasala**
- LinkedIn: [linkedin.com/in/ganasala-jaswanth](https://linkedin.com/in/ganasala-jaswanth)
- Portfolio: [jaswanthgjk.github.io](https://jaswanthgjk.github.io)
- Email: jaswanthgjk@gmail.com
