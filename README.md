# Cinema-app

## Description
This is a simulation of cinema  service for reservation tickets,
that supports registration, authentication and CRUD operations. It was written in Java and Spring.
All information is received in JSON format.

## Features
- This program supports two type of roles:
  ADMIN and USER.
- Register or login
- Create and find movies
- Create and find available movie sessions
- Create shopping cart
- Add tickets to shopping cart
- Complete an order

| Roles   | Endpoints                                                                                                                                                                                                                                                           |
|:--------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `All`   | POST: /register                                                                                                                                                                                                                                                     |
| `Admin` | GET: /cinema-halls<br/>POST: /cinema-halls<br/>GET: /movies<br/>POST: /movies<br/>GET: /movie-sessions/available<br/>POST: /movie-sessions<br/>PUT: /movie-sessions/{id}<br/>DELETE: /movie-sessions/{id}<br/>GET: /users/by-email                                  |
| `User`  | GET: /cinema-halls<br/>GET: /movies<br/>GET: /movie-sessions/available<br/>GET: /orders<br/>POST: /orders/complete<br/>PUT: /shopping-carts/movie-sessions<br/>GET: /shopping-carts/by-user                                                                         |

## Architecture
| Project structure |
| :-------- |
|`Presentation tier - Controllers`|
| `Application tier - Service` |
| `Data access tier - DAO` |

## Database structure
![diagram](img/uml.png)

## Technologies
- JDK 17
- Spring 5.3.20
- Spring Security 5.6.10
- Hibernate 5.6.14
- [MySQL](https://www.mysql.com/) 8.0.22
- [Apache Tomcat](https://tomcat.apache.org/) 9.0.50
- [Apache Maven](https://maven.apache.org/) 3.3.2

## Installation of the project:
1. Clone the project from GitHub
2. Configure /resources/db.properties with your own URL, username, password and JDBC driver
3. Configure Tomcat server (it is recommended to use version 9.0.50)
4. First user with the role of ADMIN will be created automatically with the following parameters: email - admin@i.ua, password - admin123
5. Run and enjoy the program ????
