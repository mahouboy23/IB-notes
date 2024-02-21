---
tags : mod cs
---
Created: 2024-02-21

To create a comprehensive outline for implementing the core functionalities and login for your IB Grade Management System, we'll detail each part, including tables, data types, CRUD operations, and necessary functions or methods. This guide will ensure that everything is ready for implementation.

### Database Schema

1. **Users Table** (For storing user information including teachers, students, and coordinators)
    
    - `user_id` INT AUTO_INCREMENT PRIMARY KEY
    - `username` VARCHAR(255) UNIQUE NOT NULL
    - `password` VARCHAR(255) NOT NULL
    - `role` ENUM('teacher', 'student', 'coordinator') NOT NULL
    - `full_name` VARCHAR(255) NOT NULL
2. **Classes Table** (For storing class details)
    
    - `class_id` INT AUTO_INCREMENT PRIMARY KEY
    - `class_name` VARCHAR(255) NOT NULL
    - `grade_level` ENUM('11', '12') NOT NULL
    - `subject` VARCHAR(255) NOT NULL
    - `teacher_id` INT, FOREIGN KEY REFERENCES `Users`(`user_id`)
3. **Grades Table** (For storing grades of students)
    
    - `grade_id` INT AUTO_INCREMENT PRIMARY KEY
    - `student_id` INT, FOREIGN KEY REFERENCES `Users`(`user_id`)
    - `class_id` INT, FOREIGN KEY REFERENCES `Classes`(`class_id`)
    - `grade_value` DECIMAL(5,2) NOT NULL
    - `trimester` ENUM('1', '2', '3') NOT NULL
4. **GradeBoundaries Table** (For storing grade boundaries for subjects)
    
    - `boundary_id` INT AUTO_INCREMENT PRIMARY KEY
    - `class_id` INT, FOREIGN KEY REFERENCES `Classes`(`class_id`)
    - `minimum_value` DECIMAL(5,2) NOT NULL
    - `maximum_value` DECIMAL(5,2) NOT NULL
    - `ib_grade` INT NOT NULL

### Core Functionalities & CRUD Operations

#### 1. Grade Input and Management

- **Add Grade (CREATE)**
    
    - Method: POST
    - Endpoint: `/api/grades`
    - Request Body: `{ "studentId": INT, "classId": INT, "gradeValue": DECIMAL, "trimester": ENUM }`
    - Functionality: Insert a new grade into the `Grades` table.
- **View Grades (READ)**
    
    - Method: GET
    - Endpoint: `/api/grades/student/:studentId`
    - Functionality: Retrieve all grades for a specific student.
- **Update Grade (UPDATE)**
    
    - Method: PUT
    - Endpoint: `/api/grades/:gradeId`
    - Request Body: `{ "gradeValue": DECIMAL, "trimester": ENUM }`
    - Functionality: Update a specific grade by `gradeId`.
- **Delete Grade (DELETE)**
    
    - Method: DELETE
    - Endpoint: `/api/grades/:gradeId`
    - Functionality: Remove a specific grade by `gradeId`.

#### 2. User and Class Management

- **Add User (CREATE)**
    
    - Method: POST
    - Endpoint: `/api/users`
    - Request Body: `{ "username": STRING, "password": STRING, "role": ENUM, "full_name": STRING }`
    - Functionality: Insert a new user into the `Users` table.
- **View Users (READ)**
    
    - Method: GET
    - Endpoint: `/api/users`
    - Functionality: Retrieve all users, with filters for role if needed.
- **Update User (UPDATE)**
    
    - Method: PUT
    - Endpoint: `/api/users/:userId`
    - Request Body: `{ "username": STRING, "full_name": STRING, "role": ENUM }`
    - Functionality: Update user details by `userId`.
- **Delete User (DELETE)**
    
    - Method: DELETE
    - Endpoint: `/api/users/:userId`
    - Functionality: Remove a user by `userId`.


Ok well for know i want to start and completely finish the login, session management, user part of the website. where there is a login page where you put the login details and which type of users you are then you get into you're session and have access to the "site" for your user type. know I want to further develop everything needed 
### Database Schema

1. **Users Table** (For storing user information including teachers, students, and coordinators)
    
    - `user_id` INT AUTO_INCREMENT PRIMARY KEY
    - `username` VARCHAR(255) UNIQUE NOT NULL
    - `password` VARCHAR(255) NOT NULL
    - `role` ENUM('teacher', 'student', 'coordinator') NOT NULL
    - `full_name` VARCHAR(255) NOT NULL
### Core Functionalities & CRUD Operations

#### 3. Authentication and Authorization

- **Login (CREATE Session)**
    - Method: POST
    - Endpoint: `/api/login`
    - Request Body: `{ "username": STRING, "password": STRING }`
    - Functionality: Validate user credentials against the `Users` table, and return an authentication token.
### Implementation Details

- Use bcrypt for hashing passwords before storing them in the database.
- Use JWT (JSON Web Tokens) for managing user sessions and protecting routes based on user roles.
- Implement middleware for role-based access control to restrict access to certain functionalities based on the user's role.
- Utilize Express Validator for validating and sanitizing input data to prevent SQL injection and other security threats.
- Incorporate error handling middleware in Express to handle exceptions and return appropriate HTTP status codes and messages.