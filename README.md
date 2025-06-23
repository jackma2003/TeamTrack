# TeamTrack Employee Management System 🚀

<div align="center">
  <img src="https://img.shields.io/badge/Spring%20Boot-3.0+-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" alt="Spring Boot">
  <img src="https://img.shields.io/badge/Thymeleaf-3.0+-005F0F?style=for-the-badge&logo=thymeleaf&logoColor=white" alt="Thymeleaf">
  <img src="https://img.shields.io/badge/MySQL-8.0+-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL">
  <img src="https://img.shields.io/badge/Bootstrap-5.3-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white" alt="Bootstrap">
  <img src="https://img.shields.io/badge/Java-17+-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java">
</div>

## 📋 Overview

TeamTrack is a modern, full-stack employee management system built with Spring Boot and Thymeleaf. It features a stunning dark-themed UI with animated backgrounds, providing an intuitive interface for managing employee records efficiently.

### ✨ Key Features

- 🎨 **Modern Dark UI** - Beautiful, responsive interface with animated backgrounds
- 📝 **CRUD Operations** - Complete Create, Read, Update, and Delete functionality
- 🔍 **Auto-sorted Display** - Employees automatically sorted by last name
- 📱 **Fully Responsive** - Works seamlessly on desktop, tablet, and mobile devices
- ⚡ **Fast & Efficient** - Built with Spring Boot for optimal performance
- 🛡️ **Type-safe** - Leveraging Java's strong typing system

## 🖼️ Screenshots

### Employee List View
- Clean, modern table layout
- Quick access to update and delete actions
- Animated hover effects
- Empty state handling

### Add/Update Employee Form
- Dynamic form titles based on operation
- Real-time form validation
- Smooth animations and transitions
- Loading states

## 🛠️ Tech Stack

### Backend
- **Spring Boot 3.x** - Application framework
- **Spring Data JPA** - Data persistence
- **MySQL** - Database
- **Maven** - Dependency management

### Frontend
- **Thymeleaf** - Server-side templating
- **Bootstrap 5.3** - CSS framework
- **Bootstrap Icons** - Icon library
- **Custom CSS** - Animations and dark theme

## 📦 Project Structure

```
thymeleafdemo/
├── src/main/java/com/luv2code/springboot/thymeleafdemo/
│   ├── controller/
│   │   └── EmployeeController.java     # MVC Controller
│   ├── dao/
│   │   └── EmployeeRepository.java     # Data Access Layer
│   ├── entity/
│   │   └── Employee.java               # Entity Model
│   ├── service/
│   │   ├── EmployeeService.java        # Service Interface
│   │   └── EmployeeServiceImpl.java    # Service Implementation
│   └── ThymeleafdemoApplication.java   # Main Application
├── src/main/resources/
│   ├── templates/employees/
│   │   ├── list-employees.html         # Employee List View
│   │   └── employee-form.html          # Add/Update Form
│   └── application.properties          # Configuration
└── pom.xml                             # Maven Dependencies
```

## 🚀 Getting Started

### Prerequisites

- Java 17 or higher
- Maven 3.6+
- MySQL 8.0+ (running locally)

### ⚠️ Important Note
**This application is designed to run locally on your machine.** It uses a local MySQL database and runs on `localhost:8080`. This is perfect for development, learning, or personal use.

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/teamtrack.git
   cd teamtrack
   ```

2. **Set up MySQL Database**
   
   Make sure MySQL is running locally, then create the database:
   ```sql
   CREATE DATABASE employee_directory;
   USE employee_directory;
   
   CREATE TABLE employee (
       id INT NOT NULL AUTO_INCREMENT,
       first_name VARCHAR(45) DEFAULT NULL,
       last_name VARCHAR(45) DEFAULT NULL,
       email VARCHAR(45) DEFAULT NULL,
       PRIMARY KEY (id)
   );
   ```

3. **Configure Database Connection**
   
   Update `src/main/resources/application.properties`:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/employee_directory
   spring.datasource.username=YOUR_MYSQL_USERNAME
   spring.datasource.password=YOUR_MYSQL_PASSWORD
   ```

4. **Run the Application**
   ```bash
   mvn spring-boot:run
   ```
   
   Or if using an IDE like IntelliJ IDEA or Eclipse, run the `ThymeleafdemoApplication.java` main class.

5. **Access the Application**
   
   Open your browser and navigate to: `http://localhost:8080/employees/list`
   
   📍 **Note**: The application will only be accessible on your local machine.

## 💻 Usage

### Adding an Employee
1. Click the "Add Employee" button
2. Fill in the required fields (First Name, Last Name, Email)
3. Click "Save Employee"

### Updating an Employee
1. Click the "Update" button next to any employee
2. Modify the desired fields
3. Click "Update Employee"

### Deleting an Employee
1. Click the "Delete" button next to any employee
2. Confirm the deletion in the popup dialog

## 🌐 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/employees/list` | Display all employees |
| GET | `/employees/showFormForAdd` | Show add employee form |
| GET | `/employees/showFormForUpdate?employeeId={id}` | Show update form |
| POST | `/employees/save` | Save/update employee |
| GET | `/employees/delete?employeeId={id}` | Delete employee |

## 🎨 UI Features

### Animations
- **Background Animation**: Subtle gradient shifts with rotating particles
- **Hover Effects**: Scale and color transitions on interactive elements
- **Form Animations**: Staggered fade-in effects for form fields
- **Loading States**: Smooth loading spinner during form submission

### Dark Theme Design
- Primary Background: `#0f172a`
- Secondary Background: `#1e293b`
- Primary Color: `#6366f1` (Indigo)
- Secondary Color: `#0ea5e9` (Sky Blue)
- Success Color: `#10b981` (Emerald)
- Danger Color: `#ef4444` (Red)

## 🏠 Local Development

### Running the Application
This application is designed for local development and use. After starting the application:

- **URL**: `http://localhost:8080/employees/list`
- **Port**: 8080 (default Spring Boot port)
- **Database**: Local MySQL on port 3306