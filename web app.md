---
tags : mod cs
---
Created: 2023-12-14


frontend (using React), backend (using Node.js), and a database (MySQL). Here's an outline of the structure of the project:

### Frontend (React):

#### Pages/Components:

### 1. **Login/Authentication Page:**

- **Functionality:**
    - Input fields for username and password.
    - Validation and authentication through API calls to the backend.
    - Redirect to the Dashboard upon successful login (Teacher Interface, Student Interface, Coordinator Dashboard). 
    - NO registration, the admin are the one to add users.
- **Structure:**
    - Form component for login fields.
    - Error handling for invalid credentials.
    - Integration with backend API for authentication.

### 2. **Dashboard:**

- **Functionality:**
    - Display overall statistics. to be (to be determined)
    - Navigation to different sections (Class Management, Grade Input, Bulletin(report card), Coordinator Dashboard (depends on the User)).
- **Structure:**
    - Cards or panels displaying basic info or statistics (to be determined).
    - Sidebar/Navbar for navigation.
    - Dynamic content based on user role (teacher, student, coordinator).

### 3. **Class Management:**

- **Functionality:**
    - List of students for 11th and 12th grade.
    - Access to specific class details.
    - Levels chosen (HL ou SL)
    - shows the subject (for each teacher user shows only there subject)
- **Structure:**
    - Class list component displaying (two) classes with each having the table of students.

### 4. **Grade Input page:**

- **Functionality:**
    - Grade input form per student for various subject (depends on teacher User).
    - Setting grade boundaries.
    - Shows grade average per student and for class
    - can add multiple grades to the students profile
    - and the grades are divided by trimester (three periods of grades) 
- **Structure:**
    - Forms for entering grades.
    - Settings section for grade boundaries per subject.

### 5. **Student Interface:**

- **Functionality:**
    - View grades in different formats (French, GPA, IB grading).
    - Download grade report as a PDF.
    - Access to no other functionality
- **Structure:**
    - Tabs or options for different grading formats.
    - Download button for generating PDF report.

### 6. **Coordinator/Moderator Dashboard:**

- **Functionality:**
    - Access to all data.
    - User management (add/delete users), class management, data overview.
- **Structure:**
    - Admin panel with various sections (Users, Classes, Data Overview).
    - Tables or lists for managing users and classes.

### Additional Considerations:

- **State Management:**
    - Use React Context or Redux for managing application state (user authentication, data fetching, etc.).
- **Routing:**
    - Implement React Router for page navigation and URL handling.
- **API Integration:**
    - Utilize Axios or Fetch to communicate with backend APIs for CRUD operations.
- **State Management Enhancements**:
    - For complex state management, consider using Redux Toolkit, which simplifies Redux usage.
    - Utilize React Query for efficient data fetching, caching, and synchronization with the backend.
- **User Experience (UX) Improvements**:
    - Implement lazy loading for components or routes to improve load times.
    - Use skeleton screens or loading indicators for a smoother user experience during data fetching.

### Component Breakdown:

- **Reusable Components:**
    - Header, Footer, Sidebar/Navbar for consistent layout.
    - Form components for login, grade input, etc.
    - Cards/panels for displaying statistics or class details.
    - Tables/lists for presenting data (user list, class list).

### Styling and UI/UX:

- **Design System:**
    - Maintain a consistent design system throughout the app.
    - Consider using a CSS preprocessor like SCSS for modular and maintainable styles.

### Testing and Validation:

- **Unit Testing:**
    - Write tests for components and functionalities.
    - Validate form inputs, API responses, and user interactions.

### Backend (Node.js):

#### Routes/Controllers:

### 1. **Authentication:**

- **Functionality:**
    - Verify user credentials (username/password).
    - Issue tokens upon successful login for subsequent API access.
- **Structure:**
    - Authentication middleware to validate tokens for protected routes.
    - Hashing passwords for secure storage.

### 2. **Class Management:**

- **Functionality:**
    - CRUD operations for classes (11th and 12th grade).
    - Retrieve class details, add/delete classes.
- **Structure:**
    - Routes handling GET, POST, DELETE operations for classes.
    - Controller functions for database interactions (fetching, updating, deleting classes).

### 3. **Grade Input page:**

- **Functionality:**
    - Inputting grades for students.
    - Setting grade boundaries.
- **Structure:**
    - Routes for handling grade input and boundary settings.
    - Controllers to process grade input and boundary updates.

### 4. **Student Interface:**

- **Functionality:**
    - Accessing grades in different formats (French, GPA, IB grading).
    - Generating PDF reports.
- **Structure:**
    - Routes for retrieving grades in various formats.
    - Controller functions to format and provide grade data.

### 5. **Coordinator/Moderator Access:**

- **Functionality:**
    - Access to all data.
    - User management (add/delete users), class management, data overview.
- **Structure:**
    - Specific routes for admin functionalities.
    - Controllers to manage users, classes, and overview data.

### 6. **Database Operations (MySQL):**

- **Functionality:**
    - Connect Node.js to MySQL database.
    - Execute queries for CRUD operations.
- **Structure:**
    - Use MySQL Node.js drivers (e.g., `mysql2`) to handle connections.
    - Organize SQL queries into functions/methods for reusability.

### Security Measures:

- **Input Validation and Sanitization:**
    - Validate and sanitize user inputs to prevent SQL injection or other attacks.
- **Authorization:**
    - Implement role-based access control (RBAC) for different user roles (teacher, coordinator, student).

### Error Handling and Logging:

- **Error Handling Middleware:**
    - Centralized error handling middleware for consistent error responses.
- **Logging:**
    - Implement logging mechanisms for tracking API requests, errors, and activities.

### Testing and Validation:

- **Unit Testing:**
    - Write tests for each route and controller function.
    - Validate responses, error handling, and database operations.

### Deployment and Scalability:

- **Deployment to Hosting Services:**
    - Deploy the Node.js app to platforms like Heroku, AWS, or Azure.
- **Scalability Considerations:**
    - Use best practices to ensure the app can handle increased traffic and data volume.

### Database (MySQL):

#### Tables:

### 1. **Users Table:**

- **Fields:**
    - `user_id`: Primary key
    - `username`: Unique identifier
    - `password`: Encrypted password
    - `role`: Role of the user (teacher, coordinator, student)

### 2. **Classes Table:**

- **Fields:**
    - `class_id`: Primary key
    - `class_name`: Name or identifier for the class
    - `grade_level`: Grade level (11th or 12th grade)
    - `teacher_id`: Foreign key linking to the Users table for the class teacher

### 3. **Grades Table:**

- **Fields:**
    - `grade_id`: Primary key
    - `student_id`: Foreign key linking to the Users table for the student
    - `class_id`: Foreign key linking to the Classes table
    - `subject`: Subject for which the grade is assigned
    - `grade_value`: Grade value (French, GPA, IB format, etc.)

### 4. **GradeBoundaries Table:**

- **Fields:**
    - `boundary_id`: Primary key
    - `teacher_id`: Foreign key linking to the Users table for the teacher
    - `subject`: Subject for which the boundaries are set
    - `minimum_value`: Minimum grade value for the subject
    - `maximum_value`: Maximum grade value for the subject

### Database Relationships:

- **Users ↔ Classes:**
    - One-to-Many: One teacher can be associated with multiple classes.
- **Users ↔ Grades:**
    - One-to-Many: One student can have multiple grades.
- **Users ↔ GradeBoundaries:**
    - One-to-Many: One teacher can set boundaries for multiple subjects.

### Indexes and Constraints:

- **Primary Keys:**
    - Define primary keys for each table (`user_id`, `class_id`, `grade_id`, `boundary_id`).
- **Foreign Keys:**
    - Ensure foreign keys for relational integrity among tables.
- **Unique Constraints:**
    - Ensure uniqueness where necessary (e.g., unique usernames in the Users table).

### Data Storage Considerations:

- **Secure Password Storage:**
    - Use hashing and salting techniques to store passwords securely.
- **Encryption for Sensitive Data:**
    - Encrypt sensitive information where needed to enhance security.
- **Normalization:**
    - Normalize the database to minimize redundancy and improve efficiency.

### Database Operations:

- **CRUD Operations:**
    - Create, Read, Update, and Delete operations for each table.
- **Queries for Calculations:**
    - Write queries to calculate averages, retrieve best/worst grades, and format grades into different systems.

### Backup and Recovery:

- **Regular Backups:**
    - Implement a backup strategy to prevent data loss.
- **Recovery Plan:**
    - Have a plan in place for data recovery in case of failures or corruption.

### Guide/Steps for Building:

1. **Setting Up the Database:**
    
    - Create tables using SQL queries for Users, Classes, Grades, etc.
2. **Backend Development (Node.js):**
    
    - Create API endpoints for different functionalities (authentication, class management, grading, etc.).
    - Implement database operations using MySQL queries.
3. **Frontend Development (React):**
    
    - Create components for different pages.
    - Connect frontend to backend using API calls.
4. **Integrating Authentication:**
    
    - Implement user authentication using tokens or sessions.
5. **Testing:**
    
    - Perform thorough testing of each functionality.
6. **Deployment:**
    
    - Host the backend on a server (like Heroku) and the frontend on a hosting service (like Netlify or Vercel).