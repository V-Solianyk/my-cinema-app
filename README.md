<h1 style="font-size: 42px;">CINEMA  APP</h1>

![CINEMA!](src/images/img.png)
# Summary
CinemaApp is a simple ticket booking RESTful web application that allows users to browse available movie sessions, book tickets, and manage their orders. The application supports user authentication and authorization with roles for regular users and administrators. Users can register and log in, while administrators have additional capabilities like managing cinema halls, movies, and movie sessions.

# Functionality
<h1 style="font-size: 14px;">Here is the entity relations diagram:</h1>

![DIAGRAM!](src/images/Hibernate_Cinema_Uml.png)

<h1 style="font-size: 14px;">User functionality:</h1>

- create new accounts by providing an email and password;
- log in to their accounts;
- browse the list of available cinema halls and movies;
- see the list of available movie sessions for booking;
- add movie sessions to the shopping cart and book tickets;
- view the current shopping cart and the tickets selected;
- complete ticket orders and receive confirmation;
- access the order history and past ticket bookings.

<h1 style="font-size: 14px;">Admin functionality:</h1>

- add new cinema halls and manage existing ones;
- add new movies and manage existing ones;
- add new movie sessions and manage existing ones;
- search for users by their email addresses.

# Endpoints
<h1 style="font-size: 14px;">User and Admin endpoints:</h1>

- POST: /register - user registration.
- POST: /login - user login.
- GET: /cinema-halls - view cinema halls.
- GET: /movies - view movies.
- GET: /movie-sessions/available - view available movie sessions.

<h1 style="font-size: 14px;">Admin-only endpoints:</h1>

- POST: /cinema-halls - add a new cinema hall.
- POST: /movies - add a new movie.
- POST: /movie-sessions - add a new movie session.
- PUT: /movie-sessions/{id} - update a movie session.
- DELETE: /movie-sessions/{id} - delete a movie session.
- GET: /users/by-email - find a user by email.

<h1 style="font-size: 14px;">User-only endpoints:</h1>

- GET: /orders - view user's order history.
- POST: /orders/complete - complete a ticket order.
- PUT: /shopping-carts/movie-sessions - update the shopping cart with movie sessions.
- GET: /shopping-carts/by-user - view the shopping cart for a specific user.

# Project structure
- src/main/java: contains all the source code for the application.
- src/main/resources: contains configuration files and resources.
- checkstyle/checkstyle.xml - is a configuration file for the checkstyle tool, which is used to check the code style. It contains settings for various checkstyle modules that perform various code checks for compliance with style standards;
- pom.xml - used to configure and create a Maven project, add the necessary dependencies.

# Technologies used
- JDK 17
- Spring 5.3.20
- Spring Security 5.6.10
- Hibernate 5.6.14.Final
- MySQL 8.0.22
- Maven 3.8.4
- Tomcat 9.0.76

# How to run the application
In order to launch this project, you need to take the following steps:
1. Clone this project from GitHub to your local machine.
2. Install the following software:
- Tomcat servlet container version 9.0.76;
- MySQL version 8.0 or higher;
- IntelliJ IDEA (IDE) to run the application.
- Install Postman for sending requests.
3. Open the project in IntelliJ IDEA.
4. Configure the database connection settings in the application.properties file.
5. Build the project using Maven: mvn clean package.
6. Deploy the application to Tomcat by following these steps:
- go to "Edit Configuration" in IntelliJ IDEA;
- select the installed and unzipped Tomcat version as the "Application Server";
- in the Tomcat server configuration, specify the start page that will be displayed when the application starts. Select "war exploded" and remove any unnecessary characters before the "/" sign.
7. Once the configuration is complete, click the "Run" button in IntelliJ IDEA to start the application. You can choose either normal mode or debug mode.
8. If all the steps have been followed correctly, the server will start successfully.
9. Use Postman or a web browser to interact with the endpoints and test the application.
    Please follow these instructions carefully to launch the project.