
# Student Data Entry Application (JDBC + MySQL)

This is a Java-based console application for performing CRUD (Create, Read, Update, Delete) operations on student records using a MySQL database and JDBC. It demonstrates clean object-oriented design and database integration.


---

## Project Structure

The project is modularized into four main Java classes:

- **`Main.java`**  
  Handles user input, displays the menu, and invokes appropriate functions from `StudentDAO`.

- **`Student.java`**  
  A simple POJO (Plain Old Java Object) representing a student with fields: `id`, `name`, `age`, `email`.

- **`StudentDAO.java`**  
  Contains database logic using JDBC for all CRUD operations.

- **`DBConnection.java`**  
  Manages the MySQL database connection using JDBC.

---

## Features

- Add a new student  
- Update existing student details  
- Delete a student by ID  
- List all students in the database  
- Menu-driven terminal UI

---

## Prerequisites

- Java JDK installed (v8 or higher recommended)
- MySQL server running on localhost
- MySQL user credentials configured in `DBConnection.java`

---

## Database Setup

Before running the application, create the database and the required table using the following SQL script:

```sql
CREATE DATABASE IF NOT EXISTS studentdb;

USE studentdb;

CREATE TABLE IF NOT EXISTS students (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    age INT NOT NULL,
    email VARCHAR(100) NOT NULL
);
```

---

## How to Run

1. Make sure your MySQL server is running.
2. Navigate to the project directory in the terminal.
3. Compile all the Java files:

```bash
javac *.java
```

4. Run the application:

```bash
java Main
```

