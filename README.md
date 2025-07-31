# Student_Management_System

# Student Management System (JSP + Servlets + H2 Database)

This is a full-featured Student Management System web application built using Java (JSP and Servlets), H2 Database, and Maven. It includes both **Admin** and **Student** modules for managing student data, course registration, approvals, and more.

---

## 📌 Features

### 👨‍🎓 Student Module
- Student Registration (with department selection)
- Login (only after admin approval)
- View department-specific courses
- Register for courses (max 6 per student)
- Prevent duplicate course registration
- View registered courses

### 👨‍💼 Admin Module
- Admin Login
- Approve or Decline student registrations
- View and manage approved students
- Deactivate students
- Manage Courses:
  - Add course (with department)
  - Delete course
  - Search by course name
- Manage Course Registrations:
  - View students and their courses
  - Delete any course registration

### 🔐 Logging (Log4j2)
- Logs important events like student/admin login and registration
- Console and file logging using `log4j2.xml`
- Logs stored in: `logs/app.log`

---

## 🧰 Technologies Used

| Tech         | Description                     |
|--------------|---------------------------------|
| Java         | Core application logic          |
| JSP & Servlets | Web layer                     |
| H2 Database  | Lightweight embedded database   |
| Apache Tomcat| Server (v7 used)                |
| Maven        | Dependency management           |
| Log4j2       | Logging framework               |
| Eclipse IDE  | Development environment         |

---

## ⚙️ Project Structure
src/
├── com.student.controller      # Servlets
├── com.student.dao             # DAO classes
├── com.student.model           # POJOs
├── com.student.util            # Utility classes (DBConnection)
├── com.student.test            # (Optional) Test classes
WebContent/
├── *.jsp                       # JSP files (UI)
├── WEB-INF/web.xml             # Deployment descriptor


## ⚙️ Project Setup
Prerequisites
-Java JDK 1.6 or higher (tested on JDK 1.8)

-Eclipse Luna or later

-Apache Tomcat 7 or later

-Maven 3.x

-H2 Database (embedded, no separate installation required)

#Configure Tomcat

Add Apache Tomcat 7 in Eclipse via Servers tab.

Right-click your project → Run As → Run on Server.

#Set Up Database

H2 is used in embedded mode. No installation required.

Tables like student, admin, course, registered_course, etc., will be created via the DAO during runtime or using SQL scripts.


#Add Log4j Configuration

Ensure log4j2.xml is placed under src/main/resources/.

Logs will be created in logs/app.log inside the project root directory.




