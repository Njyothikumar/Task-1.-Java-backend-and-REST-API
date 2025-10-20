
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

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
````

### 2. Build the project

```bash
mvn clean install
```

### 3. Run the application

```bash
mvn spring-boot:run
```

The server will start on:
👉 [http://localhost:8080](http://localhost:8080)

---

## 🛠️ MongoDB Configuration

Make sure MongoDB is running locally.

Update the configuration in `src/main/resources/application.properties`:

```properties
spring.data.mongodb.host=localhost
spring.data.mongodb.port=27017
spring.data.mongodb.database=Server_API
```

---

## 📁 Project Structure

```
src/
 ├── main/
 │    ├── java/          # Java source files for the main application
 │    └── resources/     # Application resource files (e.g., configuration)
 ├── test/
 │    ├── java/          # Test source files
 │    └── resources/     # Test resource files
target/                  # Compiled bytecode and build artifacts
.gitignore               # Specifies files/directories ignored by Git
pom.xml                  # Maven configuration file
README.md                # Project documentation (this file)
```

---

## Package Structure

* **com.example.serverapi.ServerController**
  REST controller classes that handle HTTP requests and responses.

* **com.example.serverapi.Server**
  Data model classes representing server entities.

* **com.example.serverapi.ServerRepository**
  Data access layer implementing MongoDB persistence logic.

* **com.example.serverapi.MongoConfig**
  Configuration classes including MongoDB setup.

---

## Configuration Files

All key configuration files, such as `application.properties`, are located in:

```
src/main/resources/
```

--

---



---

```

```


## Postman Testing

#### Add Server
![App Screenshot](1.jpg)


![App Screenshot](2.jpg)

![App Screenshot](3.jpg)

![App Screenshot](4.jpg)
