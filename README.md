# VoteVault 🗳️

**VoteVault** is a secure online voting system backend built using Spring Boot, Java, MySQL, JWT Authentication, and Spring Security. It provides REST APIs for user authentication, role-based access control, election management, candidate voting, and election results.

## 🚀 Features

- User registration and login
- JWT-based authentication
- Spring Security integration
- Role-based authorization
- Admin election management
- Election listing and details
- Candidate voting functionality
- Election results API
- Password encryption using BCrypt
- MySQL database integration
- RESTful API architecture

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Java 17 | Backend programming |
| Spring Boot | Application framework |
| Spring Security | Authentication & authorization |
| JWT | Token-based authentication |
| Spring Data JPA | Database operations |
| Hibernate | ORM |
| MySQL 8 | Database |
| Maven | Build management |

## 📁 Project Structure

```text
VoteVault/
├── src/
│   └── main/
│       ├── java/com/example/eVoting/
│       │   ├── controllers/
│       │   ├── config/
│       │   ├── entities/
│       │   ├── repositories/
│       │   └── services/
│       └── resources/
│            └── application.yml
├── pom.xml
├── mvnw
└── README.md
```

## ⚙️ Setup & Installation

### 1. Clone the repository

```bash
git clone https://github.com/KhushiJindal2006/VoteVault.git
cd VoteVault
```

### 2. Prerequisites

- Java 17
- MySQL 8
- Git

### 3. Configure MySQL

Make sure MySQL is running locally.

The application uses the `evoting` database and connects through the configuration in `application.yml`.

Set your database password as an environment variable:

**Windows PowerShell:**

```powershell
$env:DB_PASSWORD = "your_mysql_password"
```

Replace `your_mysql_password` with your local MySQL password.

### 4. Run the application

```powershell
.\mvnw.cmd spring-boot:run
```

The backend server will start at:

```text
http://localhost:8080
```

## 🔗 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | `/user/register` | Register a new user |
| POST | `/auth/login` | Authenticate user |
| POST | `/auth/logout/{username}` | Logout user |
| GET | `/user/{username}` | Get user information |
| GET | `/user/{username}/roles` | Get user roles |
| GET | `/election/all` | Get all elections |
| GET | `/election/{electionId}` | Get election details |
| GET | `/election/{electionId}/results` | Get election results |
| POST | `/admin/add/election` | Create election |
| PUT | `/admin/grant/roles/{username}` | Grant roles |
| PUT | `/admin/revoke/roles/{username}` | Revoke roles |
| POST | `/user/{username}/election/{electionId}/candidate/{candidateId}` | Cast vote |

## 🔐 Security

- JWT-based authentication
- BCrypt password hashing
- Role-based authorization
- Protected REST endpoints
- Stateless session management

## 🧪 Testing

APIs can be tested using tools such as:

- Postman
- curl

Authenticated endpoints require a valid JWT access token.

## 📌 Project Status

VoteVault is a backend-focused online voting system project developed using Spring Boot. The project demonstrates REST API development, authentication, authorization, database integration, and backend security concepts.

## 👩‍💻 Author

**Khushi Jindal**

GitHub: [KhushiJindal2006](https://github.com/KhushiJindal2006)

---

⭐ If you find this project interesting, feel free to explore the repository.