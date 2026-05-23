# TaskHub Management System

[![React](https://img.shields.io/badge/Frontend-React.js%20%2B%20Vite-61DAFB?style=flat-square&logo=react)](https://react.dev/)
[![FastAPI](https://img.shields.io/badge/Gateway-FastAPI-009688?style=flat-square&logo=fastapi)](https://fastapi.tiangolo.com/)
[![Spring Boot](https://img.shields.io/badge/Backend-Spring%20Boot-6DB33F?style=flat-square&logo=springboot)](https://spring.io/projects/spring-boot)
[![MySQL](https://img.shields.io/badge/Database-MySQL-4479A1?style=flat-square&logo=mysql)](https://www.mysql.com/)

TaskHub is a robust, full-stack task management platform built using a modern microservice-inspired architecture. It leverages **React.js** for a dynamic user experience, routing all client requests through a secure **FastAPI API Gateway**, which orchestrates communication with a high-performance **Spring Boot** core backend.

---

## 🚀 Features

- **Centralized API Gateway:** Handles routing, abstracting the core backend from the client side.
- **Dynamic User Dashboard:** Real-time task tracking, task creation, and progress visualization.
- **Secure Architecture:** Built-in decoupled service communication ready for robust token validation.
- **Responsive UI:** Tailored layout for seamless operation across desktop, tablet, and mobile displays.

---

## 🛠️ Tech Stack & Port Configuration

| Layer | Technology | Port | Description |
| :--- | :--- | :--- | :--- |
| **Frontend** | React.js (Vite) + CSS | `5173` | Client Dashboard UI |
| **API Gateway** | Python FastAPI | `8002` | Request routing & middleware hub |
| **Core Backend** | Java Spring Boot | `8001` | Business logic & data processing |
| **Database** | MySQL | `3306` | Persistent relational storage |

---

## 📂 Project Structure

```txt
TaskHub-Management-System/
├── frontend_V3/              # React Frontend application
├── backend_gatewayapi/       # FastAPI Gateway service
├── Taskhub_backend/          # Spring Boot Enterprise Backend
├── .gitignore
└── README.md

┌──────────────────┐      🚀 HTTP      ┌─────────────────────┐
│  React Frontend  │ ────────────────> │   FastAPI Gateway   │
│   (Port 5173)    │                   │     (Port 8002)     │
└──────────────────┘                   └─────────────────────┘
                                                  │
                                                  │ 🛠️ Micro-routing
                                                  ▼
┌──────────────────┐     💾 JDBC       ┌─────────────────────┐
│  MySQL Database  │ <──────────────── │ Spring Boot Backend │
│   (Port 3306)    │                   │     (Port 8003)     │
└──────────────────┘                   └─────────────────────┘


📋 Prerequisites
Before setting up the environment, ensure you have the following runtimes installed:
Node.js (v18+)
Python (3.9+)
Java JDK (17 or higher)
Maven (3.8+)
MySQL Server

⚙️ Getting Started
1. Clone the Repository
Bash
git clone [https://github.com/2500030309/TaskHub-Management-System-.git](https://github.com/2500030309/TaskHub-Management-System-.git)
cd TaskHub-Management-System-
2. Configure the Core Backend (Spring Boot)
Navigate to the database configuration file located at Taskhub_backend/src/main/resources/application.properties.

Update your MySQL database connection credentials:

Properties
   spring.datasource.url=jdbc:mysql://localhost:3306/your_database_name
   spring.datasource.username=your_mysql_username
   spring.datasource.password=your_mysql_password
🏃‍♂️ Running the Services
Note: For smooth initialization, spin up the backend components before launching the frontend interface.

🔹 Step 1: Start the Spring Boot Backend
Bash
cd Taskhub_backend
mvn spring-boot:run
The core backend will initialize at http://localhost:8001.

🔹 Step 2: Spin Up the FastAPI Gateway
Open a new terminal window:

Bash
cd backend_gatewayapi
# Create and activate virtual environment
python -m venv venv
# Windows:
venv\Scripts\activate
# Linux / macOS:
source venv/bin/activate

# Install dependencies and execute
pip install -r requirements.txt
python run.py
The gateway proxy will initialize at http://localhost:8002.

🔹 Step 3: Launch the React Frontend
Open a third terminal window:

Bash
cd frontend_V3
npm install
npm run dev
The client app will open dynamically. Access it at http://localhost:5173.

🔮 Future Roadmap
[ ] Advanced Security: Implement stateful JWT Authentication across all service borders.
[ ] Access Control: Add Role-Based Access Control (RBAC) for managers and standard users.
[ ] Containerization: Bundle services with Docker Compose for single-command deployments.
[ ] Real-time Engine: Introduce WebSockets for instant task updates across active sessions.
[ ] Automated Alerts: Build an integrated email/push notification engine.

👤 Author
Developer ID: 2500030309
GitHub Profile: @2500030309
