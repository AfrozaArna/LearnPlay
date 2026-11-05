# LearnPlay – Project Plan

## Project

**LearnPlay** is a web app where teachers or therapists create and manage interactive learning activities for children.

It's a portfolio project for a web developer internship that requires ASP.NET Core, MVC, unit testing and CI. The developer is new to ASP.NET Core, so explain each step simply.

## Features

1. **Activity management (full CRUD).** Main model: `Activity` with:
   - `Id`
   - `Title`
   - `Description`
   - `Category` (enum: `Memory`, `Language`, `MotorSkills`, `Logic`)
   - `MinAge`, `MaxAge`
   - `Difficulty` (enum: `Easy`, `Medium`, `Hard`)
   - `DurationMinutes`
   - `CreatedDate`
2. **Activity list page** with search by title and filtering by category and difficulty.
3. **Activity details page.**
4. **Validation** with data annotations (required fields, valid age range, positive duration).
5. **Dashboard page:** total activities and count per category.
6. **ASP.NET Core Identity:** only logged-in users can create, edit or delete. Anyone can view.

## Technical

- ASP.NET Core MVC (.NET 10)
- EF Core with SQLite, migrations and seed data
- Service layer `IActivityService` with dependency injection
- Bootstrap + Razor views
- Separate xUnit test project under `tests/`
- GitHub Actions workflow that builds and runs tests on every push
- Professional `README.md`

## Steps

Do one step at a time: explain it, suggest a commit message, then wait for "next".

1. [x] Solution setup
2. [ ] Models
3. [ ] Database (EF Core + SQLite)
4. [ ] Service layer
5. [ ] Controllers
6. [ ] Views
7. [ ] Identity
8. [ ] xUnit tests
9. [ ] GitHub Actions CI
10. [ ] README

At the end: 10 likely interview questions with short answers, and 2–3 sentences to describe the project on a CV.

## Development environment

- Local Windows machine: Smart App Control blocks locally built DLLs. **Do not disable it and do not use WSL.**
- Run, build and test in **GitHub Codespaces**, using `.devcontainer/devcontainer.json` (.NET 10, port 5072, C# Dev Kit).
- Run the app: `dotnet run --project src/LearnPlay.Web --launch-profile http`, then open the forwarded port 5072.
