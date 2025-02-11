Task Management Application

Overview
  This Task Management Application is built using Angular for the frontend, .NET Core Web API for the backend, and Entity Framework with SQL Server as the database. 
  The application allows create tasks, mark tasks as complete/incomplete, delete tasks, and fetch all tasks assigned to them.

Prerequisites
Ensure you have the following installed on your system:
  •	Node.js (Latest LTS version recommended)
  •	Angular CLI (npm install -g @angular/cli)
  •	.NET 8 SDK
  •	SQL Server (Local or Remote instance)
  •	Postman (Optional for API testing)

Setup and Installation
Backend (API) Setup
  1.	Clone the repository 
    git clone <repository-url>
    cd task-management-api
  2.	Configure Database 
      Update appsettings.json with your SQL Server connection string.
      "ConnectionStrings": {
          "DefaultConnection": "Server=YOUR_SERVER;Database=TaskDB;User Id=YOUR_USER;Password=YOUR_PASSWORD;"
      }
  3.	Apply Migrations and Seed Database 
    dotnet ef database update
  4.	Run the API 
    dotnet run
The API should be running at http://localhost:5000.

Frontend (Angular) Setup
  1.	Navigate to the Angular project 
    cd task-management-ui
  2.	Install dependencies 
    npm install
  3.	Run the application 
    ng serve
The frontend should be accessible at http://localhost:4200.

Assumptions
  •	The application assumes basic CRUD operations for task management.

Design Decisions
1.	Frontend (Angular)
  o	Used Angular for UI components.
  o	Implemented reactive forms for task creation.
  o	Used Angular services to handle API calls.
2.	Backend (.NET Core Web API)
  o	Followed RESTful API principles.
  o	Used Entity Framework Core for database operations.
  o	Applied global exception handling and logging.
3.	Database (SQL Server with Entity Framework Core)
  o	Used Code-First approach.
  o	Created tables for  TaskDetails.
