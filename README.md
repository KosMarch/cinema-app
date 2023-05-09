<img src="https://user-images.githubusercontent.com/115244741/237032461-3b2f1f9c-98b6-4756-8240-bc5974c83330.png" width="300" height="300">
 
 # 🎬 CINEMA APP
Cinema App is a simple web application built using standard Spring and Hibernate frameworks. It allows users to view information about cinema halls, films, screenings and book tickets. There is also an administrator role that has the right to manage the application. The program is easy to use and offers a wide range of functionality.


## ⚙ Features 
- Register a new user
- Login (username and password)
- Role-based authorization (admin, user)
- Exception handling (invalid username, password, invalid role) with descriptive messages
- Project has multiple endpoints with user and admin access
    - POST: `/register` (to create a user) - `ALL`
    - POST: `/cinema-halls` (to create a cinema hall) - `ADMIN`
    - POST: `/movies` (to create a movie) - `ADMIN`
    - POST: `/movie-sessions` (to create a movie session) - `ADMIN`
    - POST: `/orders/complete` (to create an order for the current user) - `USER`
    - PUT: `/movie-sessions/{id}` (to update a movie session) - `ADMIN`
    - PUT: `/shopping-carts/movie-sessions` (to add movie session to the shopping cart) - `USER`
    - DELETE: `/movie-sessions/{id}` (to delete a movie session) - `ADMIN`
    - GET: `/orders` (to get order history for the current user) - `USER`
    - GET: `/shopping-carts/by-user` (to get a shopping cart for the current user) - `USER`
    - GET: `/cinema-halls` (to get all cinema halls) - `USER` or `ADMIN`
    - GET: `/movies` (to get all movies) - `USER` or `ADMIN`
    - GET: `/movie-sessions/available` (to get all available movies by date) - `USER` or `ADMIN`
    - GET: `/users/by-email` (to find user by email) - `ADMIN`

## 📃 Structure
* `controller` - contains controllers for endpoints with different access depending on the role
* `config` - stores Spring and App configuration
* `dao` - data access layer (repository) with CRUD methods in the database
* `dto` - wrapper for model objects to unify the requests and responses in controllers
* `exception` - custom exception class for DAO's exceptions 
* `lib` - contains email and password validators with its annotations
* `model` - contains models of entity for the database
* `service` - contains services that call repositories and perform business logic
* `mapper` - сonverts model objects into DTO objects and vice versa
* `util` - utility class used in a project to save DateTime pattern
* `resources` - contains properties for database

### Completed structure of project:

<img src="https://user-images.githubusercontent.com/115244741/237047897-81d4117f-3b3a-4fe6-ae75-795990ece54e.png" width="700" height="500">

## 💾 Getting Started
-  Clone the project repository to your local machine.
-  Configure the database connection parameters in the `resources/db.properties` file.
-  Set up a local Tomcat configuration in your IDE.
-  Run the Tomcat configuration and deploy the application.
-  Access the application using the specified URL.
-  Use the provided credentials to test the application's functionalities.

## 🚀 Used technologies
- Java 17
- Apache Maven
- Apache Tomcat
- MySQL
- Hibernate
- Spring:
    - Core
    - Web Mvc
    - Security

### Author
[Kostiantyn Marchenko](https://github.com/KosMarch)
