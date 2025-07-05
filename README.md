# 🐾 Meowmentum – Backend API

Welcome to the **Meowmentum Backend API**, the central engine behind our AI-powered English–Vietnamese language learning platform.  
Built with **C# and ASP.NET Core (.NET 8)**, this backend handles user authentication, vocabulary content management, learning progress tracking, and provides APIs for future AI and mobile/web integrations.

> 🔗 Full project ecosystem: [Meowmentum Overview](https://github.com/meowmentum-education)

---

## 🛠️ Tech Stack

| Layer            | Technologies                         |
|------------------|--------------------------------------|
| Framework        | ASP.NET Core (.NET 8)                |
| Language         | C# 11                                |
| API Architecture | RESTful APIs                         |
| ORM              | Entity Framework Core 8              |
| Database         | Microsoft SQL Server                 |
| Authentication   | JWT Bearer Token                     |
| API Docs         | Swagger UI (Swashbuckle.AspNetCore)  |
| CI/CD            | GitHub Actions                       |
| Containerization | Docker (planned)                     |

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
├── Config/            # Constants & custom settings
├── Program.cs         # Main entry point
└── appsettings.json   # Environment configurations
```

---

## 🚀 Getting Started

### 📦 Prerequisites

- [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0)
- SQL Server (LocalDB / Docker / Cloud)
- Visual Studio 2022+ or VS Code with C# extensions

### 🔧 Setup

1. **Clone the repository**

```bash
git clone https://github.com/trandaine/meowmentum-backend.git
cd meowmentum-backend
```

2. **Configure the database connection**

In `appsettings.Development.json`:

```json
"ConnectionStrings": {
  "DefaultConnection": "Server=localhost;Database=MeowmentumDb;Trusted_Connection=True;"
}
```

3. **Apply EF Core migrations**

```bash
dotnet ef database update
```

4. **Run the API**

```bash
dotnet run
```

Visit the API:

- `https://localhost:5001`
- `http://localhost:5000`

Swagger UI:

- `https://localhost:5001/swagger`

---

## 🔐 Authentication

- Implements **JWT Bearer Authentication**
- Add this header to authorized requests:

```http
Authorization: Bearer {your_token_here}
```

---

## 🔑 Key Features

- 👤 Secure Registration & Login (bcrypt + JWT)
- 📚 Vocabulary & Topic Management (CRUD)
- 📈 Learning Progress & Quiz Results Tracking
- 🧠 AI Endpoint Hooks (for Django NLP microservice)
- 🛡️ Admin Content Panel (WIP)

---

## 🧪 Testing

Tests (if configured) are under `/Tests`

To run tests:

```bash
dotnet test
```

---

## 📦 Deployment

- CI/CD via GitHub Actions
- Docker support in progress (`Dockerfile`)
- Use environment variables for production secrets

---

## 🤝 Contributing

1. Fork this repository
2. Create a new branch
3. Make changes and commit
4. Open a pull request 🚀

Please follow our clean architecture and REST API conventions.

---

## 📬 Maintainer

- 👤 **Trần Quang Đại** – Backend Engineer  
  📧 `daitqgcs220714@fpt.edu.vn`  
  GitHub: [@trandaine](https://github.com/trandaine)

---

> *Meowmentum – intelligent, scalable, and learner-centered English education.*

---