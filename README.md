# 🍽️ Smart Meal Planner System

A **3-layer architecture** backend system built with C# and ASP.NET Core that helps users plan meals, track nutritional intake, and manage their weekly diet efficiently.

---

## 📁 Project Structure

```
Smart-Meal-Planner-System/
├── PresentationAPI/           # ASP.NET Core Web API — controllers & endpoints
├── BLL/                       # Business Logic Layer — services & rules
├── DAL/                       # Data Access Layer — database operations
├── MealPlanner.sln            # Visual Studio solution file
└── README.md
```

---

## 🏗️ Architecture Overview

This project follows a clean **3-Layer Architecture** pattern, separating concerns across three distinct layers:

| Layer | Project | Responsibility |
|---|---|---|
| Presentation | `PresentationAPI` | Exposes REST API endpoints, handles HTTP requests & responses |
| Business Logic | `BLL` | Core application rules, validation, service logic |
| Data Access | `DAL` | Database interactions, repository pattern, Entity Framework |

```
Client Request
      ↓
 PresentationAPI   ←→   Controllers / API Routes
      ↓
     BLL           ←→   Services / Business Rules
      ↓
     DAL           ←→   Repositories / Database
```

---

## 🧠 Concepts Demonstrated

| Concept | Where Used |
|---|---|
| 3-Layer Architecture | Full solution structure |
| REST API design | `PresentationAPI` — HTTP endpoints |
| Service layer pattern | `BLL` — business logic separation |
| Repository pattern | `DAL` — data access abstraction |
| Dependency Injection | Cross-layer wiring via .NET DI container |
| Entity Framework / ORM | `DAL` — database operations |

---

## ⚙️ Features

- Meal planning and weekly schedule management
- Nutritional information tracking per meal
- Ingredient and grocery list management
- Diet preference and calorie goal support
- RESTful API for frontend or mobile integration

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| C# / .NET | Core language & runtime |
| ASP.NET Core Web API | REST API framework |
| Entity Framework Core | ORM & database access |
| SQL Server | Relational database |
| Visual Studio 2022 | IDE |

---

## ▶️ How to Run

### Prerequisites
- SQL Server (local or remote)
- Visual Studio 2022 or VS Code

### Steps

1. Clone the repository:
```bash
git clone https://github.com/<your-username>/Smart-Meal-Planner-System.git
cd Smart-Meal-Planner-System
```

2. Open `MealPlanner.sln` in Visual Studio

3. Update the connection string in `PresentationAPI/appsettings.json`:
```json
"ConnectionStrings": {
  "DefaultConnection": "Server=YOUR_SERVER;Database=MealPlannerDB;Trusted_Connection=True;"
}
```

4. Apply database migrations:
```bash
cd DAL
dotnet ef database update
```

5. Run the API:
```bash
cd PresentationAPI
dotnet run
```

6. Open your browser and navigate to:
```
https://localhost:5001/swagger
```

---

## 📂 .gitignore Recommendation

Make sure your `.gitignore` excludes build artifacts before pushing:

```gitignore
# Build output
bin/
obj/

# Visual Studio
.vs/
*.user

# Local settings
appsettings.Development.json
```

---
