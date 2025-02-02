# Employee Management System with JavaFX

An Employee Management System built with **JavaFX** and **MySQL**. This application provides a graphical interface to manage employee records, including creating, viewing, and updating employee data in a relational database.

## Table of Contents
1. [Overview](#overview)  
2. [Features](#features)  
3. [Technologies Used](#technologies-used)  
4. [Prerequisites](#prerequisites)  
5. [Installation](#installation)  
6. [Usage](#usage)  
7. [Database Setup](#database-setup)  
8. [Project Structure](#project-structure)  
9. [Contributing](#contributing)  
10. [License](#license)

---

## Overview

**Employee Management System with JavaFX** is a simple yet powerful desktop application that simplifies the process of handling employee data. The goal of this project is to demonstrate **CRUD** (Create, Read, Update, Delete) operations and an easy-to-use UI, making it a solid starting point for learning or extending with more features.

- **Create**: Add new employees (name, age, email, department).  
- **Read**: View the entire list of employees.  
- **Update**: Edit existing employee records using their unique ID.

This repository contains Java source files and SQL scripts required to set up the employee database.

---

## Features

- **JavaFX UI**: Clean and intuitive user interface for managing employees.
- **MySQL Database Integration**: Leverages JDBC to communicate with a MySQL database.
- **CRUD Operations**: Allows insertion, retrieval, and update of records.
- **Automatic Table Creation**: Creates necessary database tables if they don't exist.

---

## Technologies Used

- **Java 8+**
- **JavaFX**
- **MySQL**
- **JDBC**
- **Git/GitHub** for version control

---

## Prerequisites

Before running this application, ensure you have the following installed:

- **Java JDK 8 or higher**
- **MySQL Server**
- **Maven** or another build tool (optional; you can also compile manually)

---

## Installation

1. **Clone the Repository**  
   ```bash
   git clone https://github.com/<YourUsername>/Employee-Management-System-with-JavaFX.git
2. **Open in Your IDE**  
   Import the project into your favorite IDE (IntelliJ, Eclipse, NetBeans, etc.).

3. **Configure MySQL Credentials**  
   In the `EmployeeDatabase.java` file, update the following constants if your MySQL setup differs:
   ```java
   private static final String URL = "jdbc:mysql://localhost:3306/employeeDB";
   private static final String USER = "root";
   private static final String PASSWORD = "753426";
Adjust these properties based on your MySQL configuration.

---

## Usage

1. **Build and Run**
- You can run the `EmployeeManager` class directly from your IDE.
- Alternatively, compile from the command line (replace paths as necessary):
  ```bash
  javac com/example/demo/*.java
  java com.example.demo.EmployeeManager
2. **Application Workflow**

- **On launching the app**, a window opens with text fields for *Employee ID*, *Name*, *Age*, *Email*, and *Department*.
- **Add Employee**: Provide the necessary information (excluding ID) and click **Add Employee**.
- **View Employees**: Click **View Employees** to print a list of all employees in the console.
- **Update Employee**: Enter the **Employee ID** and the new details to update a specific record.

---

## Database Setup

1. **Create Database**  
   From your MySQL command line or client (e.g., MySQL Workbench), run:
   ```sql
   CREATE DATABASE employeeDB;
   USE employeeDB;
2. **Automatic Table Creation**

When the application runs, it will attempt to create the `employees` table if it does not exist.

**Note**: For any advanced customization or manual table creation, refer to `employeedatabase.sql` or the SQL in `createNewTable()` in the `EmployeeDatabase` class.

---

## Project Structure

```pgsql
Employee-Management-System-with-JavaFX
├── com
│   └── example
│       └── demo
│           ├── EmployeeDatabase.java
│           └── EmployeeManager.java
├── employeedatabase.sql
└── README.md

- **EmployeeDatabase.java**: Contains the JDBC logic for connecting to the MySQL database, creating tables, and handling CRUD operations.  
- **EmployeeManager.java**: A JavaFX application that provides a graphical interface to interact with the backend.  
- **employeedatabase.sql**: SQL commands for database creation (optional manual setup).

---

