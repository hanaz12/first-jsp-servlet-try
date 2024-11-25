# User Management Application

This is a simple **User Management Application** built using **JSP** (JavaServer Pages) and **Servlets**. It allows you to perform basic CRUD (Create, Read, Update, Delete) operations on users. The application uses a MySQL database to store user information such as name, email, and country.

## Features

- **Add new user**: Add a new user by providing their name, email, and country.
- **List users**: View all users in a tabular format with options to edit or delete.
- **Edit user**: Update the user's information.
- **Delete user**: Remove a user from the list.

## Tech Stack

- **Frontend**: JSP, HTML, Bootstrap
- **Backend**: Java Servlets
- **Database**: MySQL (or any relational database of your choice)

## Prerequisites

- JDK (Java Development Kit) version 8 or above
- Apache Tomcat (or any Java-based servlet container)
- MySQL (or any relational database)
- Git

## Getting Started

1. **Clone the repository**:
    ```bash
    git clone https://github.com/hanaz12/first-jsp-servlet-try.git
    ```

2. **Setup MySQL Database**:
    - Create a database (e.g., `userdb`).
    - Use the `UserDAO` class to connect to your database.
    - Make sure to create the table to store user data, like:
    ```sql
    CREATE TABLE users (
        id INT PRIMARY KEY AUTO_INCREMENT,
        name VARCHAR(255) NOT NULL,
        email VARCHAR(255) NOT NULL,
        country VARCHAR(255) NOT NULL
    );
    ```

3. **Deploy the project**:
    - Open the project in your favorite IDE (e.g., IntelliJ IDEA, Eclipse).
    - Build and deploy the project to Apache Tomcat.
    - Run the project on `http://localhost:8080/`.

4. **Use the application**:
    - Visit `http://localhost:8080/jspservletproject/list` to see the list of users.
    - You can add, edit, or delete users from this page.

## File Structure

- **WebContent/**
  - `user-list.jsp` – Lists all the users with options to edit and delete.
  - `user-form.jsp` – A form to add or edit a user.
  - `WEB-INF/web.xml` – Servlet configuration.
- **src/**
  - `dao/UserDAO.java` – Data Access Object for interacting with the database.
  - `model/User.java` – Model class representing the User entity.
  - `web/UserServlet.java` – Servlet for handling requests and business logic.

## License

This project is open source and available under the [MIT License](LICENSE).
