Banking Management System

A Banking Management System built with C# and .NET, consisting of a RESTful Web API backend and a Windows Forms desktop client.

The project follows a layered architecture to separate business logic, data access, and user interface responsibilities.

Architecture

The project consists of two main applications:

- Bank Backend (Server): An ASP.NET Core Web API responsible for handling business operations, database interactions, authentication, and authorization.
- Bank UI (Client): A Windows Forms desktop application that communicates with the backend through HTTP requests and consumes its RESTful APIs.

Technologies Used

- C#
- .NET / ASP.NET Core Web API
- Windows Forms (WinForms)
- Entity Framework Core
- SQL Server
- RESTful APIs
- JWT Authentication
- Refresh Token Mechanism
- Dependency Injection

Key Features

- User authentication and session management.
- JWT-based authentication with refresh token support.
- Role/permission-based authorization.
- Client and user management.
- Bank account management.
- Account operations and transaction management.
- Separation of concerns using a layered architecture.
- HTTP communication between the desktop client and backend API.

Project Structure

Banking Management System
│
├── Bank Backend
│   ├── API Layer
│   ├── Business Layer
│   └── Data Access Layer
│
└── Bank UI
    ├── Forms
    ├── Services
    └── Authentication & Session Management

Demo

A video demonstrating the application in action is available here:

"Watch Project Demo" ()

Getting Started

1. Clone the repository.
2. Configure the SQL Server connection string in the backend.
3. Configure the API base address in the desktop client.
4. Apply the database migrations or use the provided database setup.
5. Run the backend API.
6. Run the Windows Forms client.

---

Note: The desktop client requires the backend API to be running to perform banking operations.
