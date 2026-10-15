# Project Backend

Spring Boot REST API and MySQL persistence for the Smart Study Planner.

## Requirements

- Java 17+
- Maven 3.9+
- MySQL 8+

## Configure and run locally (PowerShell)

Set your local database credentials in the shell; do not commit them:

```powershell
$env:DB_URL = "jdbc:mysql://localhost:3306/smartstudyplanner?createDatabaseIfNotExist=true&useSSL=false&serverTimezone=UTC"
$env:DB_USERNAME = "root"
$env:DB_PASSWORD = "your-local-password"
$env:FRONTEND_ORIGIN = "http://localhost:5173"
mvn spring-boot:run
```

The API listens on `http://localhost:8080`. `GET /` is a health message; `GET /api/subjects` lists subjects and `POST /api/subjects` creates one. `FRONTEND_ORIGIN` defaults to `http://localhost:5173`; set it to the exact deployed frontend origin elsewhere.

Database settings are provided through `DB_URL`, `DB_USERNAME`, and `DB_PASSWORD`. No password or deployment secret is stored in this repository.

## Checks

```powershell
mvn test
```
