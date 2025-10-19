# 🚀 Server Management API

A Java-based REST API built with **Spring Boot** and **MongoDB** for managing "server" objects. The application allows users to **create**, **retrieve**, **search**, and **delete** server records via HTTP endpoints.

This project is ideal for learning REST API development with Java Spring Boot and MongoDB integration.

---

## 📚 Table of Contents

- [✅ Prerequisites](#-prerequisites)
- [⚙️ Project Setup](#️-project-setup)
- [🛠️ MongoDB Configuration](#️-mongodb-configuration)
- [📁 Project Structure](#-project-structure)
- [📡 API Endpoints](#-api-endpoints)
- [🧪 Postman Testing](#-postman-testing)
- [📄 License](#-license)

---

## ✅ Prerequisites

Ensure the following are installed on your system:

- Java JDK 17+
- Maven
- MongoDB (running locally or via MongoDB Atlas)
- Postman (for testing the API)

---

## ⚙️ Project Setup

### 1. Clone the repository

bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
2. Build the project
bash
Copy code
mvn clean install
3. Run the application
bash
Copy code
mvn spring-boot:run
The server will start on:
👉 http://localhost:8080

🛠️ MongoDB Configuration
Make sure MongoDB is running locally.

Update the configuration in src/main/resources/application.properties:

properties
Copy code
spring.data.mongodb.host=localhost
spring.data.mongodb.port=27017
spring.data.mongodb.database=Server_API
📁 Project Structure
plaintext
Copy code
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com.example.serverapi/
│   │   │       ├── ServerController/       # REST API controllers
│   │   │       ├── Server/                 # Server model (POJO)
│   │   │       ├── ServerRepository/       # MongoDB repository
│   │   │       └── MongoConfig/            # (Optional) DB config
│   │   └── resources/
│   │       └── application.properties      # Configurations
│   └── test/                               # Unit and integration tests
├── pom.xml                                 # Maven build file
└── README.md                               # Project documentation
📡 API Endpoints
1. 🟢 Create Server - POST /api/servers
Request Body:

json
Copy code
{
  "id": "123",
  "name": "Amrita CentOS",
  "language": "Java",
  "framework": "Spring Boot"
}
2. 🔵 Get All Servers - GET /api/servers
Returns a list of all server objects.

3. 🔍 Get Server by ID - GET /api/servers/{id}
Retrieves a server by its unique ID.

4. ❌ Delete Server by ID - DELETE /api/servers/{id}
Deletes a specific server using its ID.

5. 🔎 Find Server by Name - GET /api/servers/findByName?name={searchText}
Searches for servers whose name contains the given query string (case-insensitive).

## Testing With Postman

#### Create Server
![App Screenshot](https://drive.google.com/uc?id=1ezt912aEXuSkapDF9qfan7BTS-NpIqp7)

![App Screenshot](https://drive.google.com/uc?id=1p0iGF1t3Rc0apF43wAnWWqF4eG1Yt9PT)


#### Get all Servers
![App Screenshot](https://drive.google.com/uc?id=1eJEaYdNRP7zDD-3HA-fgTLTUXMtebZ5t)


#### Get Server by ID
![App Screenshot](https://drive.google.com/uc?id=15Y4E53wPiE3-QDY7h9m0O48aN3KWIuXL)



#### Find Servers by Name
![App Screenshot](https://drive.google.com/uc?id=19Q0BTA1mREzUyAmpQmfu1xv4f5gaJUyl)


#### Delete Server by ID
![App Screenshot](https://drive.google.com/uc?id=1bIiLpAWRTenqYNuLOBWuNp8ML5xsTAhG)
