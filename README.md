🚀 Server Management API

A Java-based REST API built with Spring Boot and MongoDB for managing "server" objects. The application allows users to create, retrieve, search, and delete server records via HTTP endpoints.

This project is intended for learning REST API development, Java Spring Boot, and MongoDB integration.

📚 Table of Contents

Prerequisites

Project Setup

MongoDB Configuration

Project Structure

API Endpoints

Create Server

Get All Servers

Get Server by ID

Delete Server by ID

Find Server by Name

Postman Testing

License

✅ Prerequisites

Before running this project, ensure you have the following installed:

Java JDK 17+

Maven

MongoDB

Postman
 (for testing)

⚙️ Project Setup

Clone the repository:

git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>


Build the project:

mvn clean install


Run the application:

mvn spring-boot:run


By default, the app runs on:
http://localhost:8080

🛠️ MongoDB Configuration

Ensure MongoDB is running locally on your machine. Configure the database settings in src/main/resources/application.properties:

spring.data.mongodb.host=localhost
spring.data.mongodb.port=27017
spring.data.mongodb.database=Server_API

📁 Project Structure
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com.example.serverapi/
│   │   │       ├── ServerController/       # REST controller
│   │   │       ├── Server/                 # Server model
│   │   │       ├── ServerRepository/       # MongoDB repository
│   │   │       └── MongoConfig/            # (Optional) Mongo config
│   │   └── resources/
│   │       └── application.properties
│   └── test/                               # Test classes
├── target/                                 # Compiled files
├── pom.xml                                 # Maven dependencies
└── README.md                               # Project guide

📡 API Endpoints
1. 🟢 Create Server [POST]

URL: /api/servers
Body:

{
  "id": "123",
  "name": "Amrita",
  "language": "Java",
  "framework": "Django"
}

2. 🔵 Get All Servers [GET]

URL: /api/servers
Returns a list of all servers.

3. 🔍 Get Server by ID [GET]

URL: /api/servers/{id}
Returns a single server by its ID.

4. ❌ Delete Server by ID [DELETE]

URL: /api/servers/{id}
Deletes the server with the specified ID.

5. 🔎 Find Server by Name [GET]

URL: /api/servers/findByName?name={searchText}
Searches for servers where the name contains the given text (case-insensitive).

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
