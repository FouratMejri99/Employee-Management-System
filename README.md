# Employee Management System

## Overview
The Employee Management System (EMS) is a web-based application designed to streamline HR operations such as employee record management, attendance tracking, and payroll processing. The system provides an intuitive interface for HR personnel and managers to manage employee data efficiently.

## Features
- Employee profile management (add, edit, delete employees)
- Attendance tracking
- Payroll management
- Role-based authentication and access control
- Reporting and analytics
- Department-wise employee categorization

## Technologies Used
- **Frontend**: Angular (Material Design for UI components)
- **Backend**: Spring Boot
- **Database**: MySQL (JPA/Hibernate ORM)
- **Authentication**: JSON Web Token (JWT)
- **Deployment**: AWS (Frontend), Heroku (Backend)

## Installation

### Prerequisites
Ensure you have the following installed:
- Node.js (LTS version recommended)
- MySQL (local or cloud instance)
- Java 11 or later
- Git

### Steps
1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/employee-management-system.git
   cd employee-management-system
   ```
2. Install dependencies for the backend:
   ```sh
   cd backend
   mvn clean install
   ```
3. Install dependencies for the frontend:
   ```sh
   cd ../frontend
   npm install
   ```
4. Configure environment variables:
   - Create a `application.properties` file in the `backend/src/main/resources` folder with the following:
     ```properties
     spring.datasource.url=jdbc:mysql://localhost:3306/ems
     spring.datasource.username=root
     spring.datasource.password=yourpassword
     spring.jpa.hibernate.ddl-auto=update
     jwt.secret=your_jwt_secret
     server.port=8080
     ```
5. Start the backend server:
   ```sh
   cd backend
   mvn spring-boot:run
   ```
6. Start the frontend:
   ```sh
   cd frontend
   ng serve
   ```
7. Open the application in your browser at `http://localhost:4200`

## API Endpoints
### Authentication
- `POST /api/auth/login` - User login
- `POST /api/auth/register` - Register a new user

### Employees
- `GET /api/employees` - Get all employees
- `POST /api/employees` - Add a new employee
- `PUT /api/employees/:id` - Update employee details
- `DELETE /api/employees/:id` - Remove an employee

## Contribution Guidelines
1. Fork the repository.
2. Create a new branch for your feature/bug fix.
3. Commit your changes with descriptive messages.
4. Push the branch and create a pull request.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Contact
For any issues or inquiries, please contact [your email] or open an issue in the repository.

