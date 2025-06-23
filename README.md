# 🐾 Meowmentum – Backend API

Welcome to the **Meowmentum Backend API**, the central engine of an AI-enhanced English language learning platform. Built with **C# and ASP.NET Core (.NET 8)**, this backend manages user authentication, vocabulary data, learning analytics, and API endpoints for future AI integration.

> 🔗 See the full project vision: [Meowmentum Overview](https://github.com/meowmentum-education)

---

## 🛠️ Tech Stack

| Layer          | Technologies                     |
|----------------|----------------------------------|
| Framework      | ASP.NET Core (.NET 8)            |
| Language       | C# 11                            |
| API Type       | RESTful APIs                     |
| ORM            | Entity Framework Core 8          |
| Database       | Microsoft SQL Server             |
| Auth           | JWT Bearer Authentication        |
| Docs           | Swagger UI (Swashbuckle.AspNetCore) |
| DevOps         | GitHub Actions                   |
| Containerization | Docker (planned)              |

---

## 📁 Project Structure

```
/Meowmentum.API
├── Controllers/       # API endpoints
├── Models/            # EF entities
├── DTOs/              # Request/response types
├── Services/          # Business logic
├── Repositories/      # Data access layer
├── Middleware/        # Auth, error handling, logging
├── Config/            # Configuration files and constants
├── Program.cs         # Entry point using top-level statements
└── appsettings.json   # Environment settings
```

---

## 🚀 Getting Started

### 📦 Prerequisites

- [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0)
- SQL Server (LocalDB, Docker, or cloud)
- Visual Studio 2022+ or Visual Studio Code

### 🔧 Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/trandaine/meowmentum-backend.git
   cd meowmentum-backend
   ```

2. **Configure connection string**

   In `appsettings.json` or `appsettings.Development.json`:

   ```json
   "ConnectionStrings": {
     "DefaultConnection": "Server=localhost;Database=MeowmentumDb;Trusted_Connection=True;"
   }
   ```

3. **Run EF Core migrations**

   ```bash
   dotnet ef database update
   ```

4. **Run the API**

   ```bash
   dotnet run
   ```

   Access the API at:
   - `https://localhost:5001`
   - `http://localhost:5000`

5. **API Docs (Swagger)**  
   Navigate to: `https://localhost:5001/swagger`

---

## 🔐 Authentication

- Token-based authentication via **JWT**.
- Example header:

```http
Authorization: Bearer {your_token_here}
```

---

## 🔑 Key Features

- ✅ User Registration & Login (with password hashing & JWT)
- 📚 Vocabulary Management by Topics & CEFR Level
- 📈 Progress Tracking & Quiz History
- 🧠 AI Module Hooks (for integration with Django NLP microservice)
- 🛡️ Admin-level Content Management (WIP)

---

## 🧪 Testing

Tests are placed under the `/Tests` directory (if configured).

Run all tests:

```bash
dotnet test
```

---

## 📦 Deployment

- CI/CD with GitHub Actions (`.github/workflows`)
- Dockerfile support (in progress)
- Environment variables recommended for production secrets

---

## 🤝 Contributing

1. Fork this repo
2. Create your feature branch
3. Commit and push
4. Open a pull request 🚀

Please follow our coding standards and API conventions.

---

## 📬 Maintainers

- 👤 **Trần Quang Đại** – Backend Engineer  
  📧 `daitqgcs220714@fpt.edu.vn`  
  GitHub: [@trandaine](https://github.com/trandaine)

---

> *Meowmentum – intelligent, scalable, and learner-centered English education.*

---