# 🏋️ Fitness Training Platform

A Java Web Application built using Servlets, JSP, JDBC, and MySQL that allows users to follow workout plans, track fitness progress, and interact with trainers. Administrators manage users and approve workout plans.

This project follows MVC architecture and is suitable for college mini-projects, labs, and viva examinations.

# 📌 Features Overview

Role-Based Authentication

Secure login system

Roles fetched from database (ADMIN, TRAINER, USER)

Role-based dashboards

Session management and logout functionality

# 👥 User Roles & Functionalities
## 👨‍💼 Admin

View admin dashboard

Approve or reject workout plans submitted by trainers

Manage users (via separate JSP pages)

Secure access using session-based role validation

## 🧑‍🏫 Trainer

Create workout plans

Submit plans for admin approval

Access trainer-specific dashboard

## 🧑‍🚴 User

View user dashboard

Enter fitness progress (weight, measurements)

View progress analytics using charts

Secure logout

# 📊 Fitness Progress Visualization

Progress data stored in MySQL

Weight progress visualized using Chart.js

Separate analytics page (progressChart.jsp)

Clean and responsive UI

# 🛠️ Technology Stack
```
Layer	Technology
Frontend:	JSP, HTML, CSS
Backend:	Java Servlets
Database:	MySQL
Connectivity:	JDBC
Server:	Apache Tomcat 9
Charts:	Chart.js
IDE	Eclipse
```
# 🧱 Project Architecture (MVC)
View       → JSP Pages  
Controller → Servlets  
Model      → DAO + Database

JSP handles UI

Servlets handle business logic

DAO handles database operations

MySQL stores persistent data

# 📁 Project Structure
```
FitnessTrainingPlatform/
│
├── src/main/java/com/fitness/
│   ├── controller/
│   │   ├── LoginServlet.java
│   │   ├── LogoutServlet.java
│   │   ├── admin/WorkoutApprovalServlet.java
│   │   ├── trainer/WorkoutPlanServlet.java
│   │   └── user/ProgressServlet.java
│   │
│   ├── dao/
│   │   ├── UserDAO.java
│   │   ├── WorkoutPlanDAO.java
│   │   └── ProgressDAO.java
│   │
│   └── util/
│       └── DBConnection.java
│
├── src/main/webapp/
│   ├── jsp/
│   │   ├── login.jsp
│   │   ├── admin/
│   │   │   ├── adminDashboard.jsp
│   │   │   └── manageWorkouts.jsp
│   │   ├── trainer/
│   │   │   └── trainerDashboard.jsp
│   │   └── user/
│   │       ├── userDashboard.jsp
│   │       └── progressChart.jsp
│   │
│   └── WEB-INF/
│       └── web.xml
│
├── database/
│   └── fitness_db.sql
│
└── README.md
```
# 🗄️ Database Tables

users

workout_plans

progress

messages

Sample data is provided for:

Admin, Trainer, and User accounts

Workout plans (pending & approved)

Progress tracking

# ▶️ How to Run the Project
## 1️⃣ Prerequisites

Java 17 (recommended)

Apache Tomcat 9

MySQL Server

Eclipse IDE

## 2️⃣ Database Setup
CREATE DATABASE fitness_db;
USE fitness_db;
-- Run fitness_db.sql

## 3️⃣ Project Setup in Eclipse

Create a Dynamic Web Project

Copy source files into the project

Add MySQL Connector JAR to WEB-INF/lib

Configure Java 17 as project JRE

Add project to Tomcat server

## 4️⃣ Run the Application
http://localhost:8080/<project-name>/

(Default page opens login.jsp)

# 🔐 Sample Login Credentials
```
Role	      Email	          Password
Admin	   admin@test.com     admin123
Trainer	 trainer1@test.com  trainer123
User	   user1@test.com     user123
```
# 🔒 Security Measures

Session-based authentication

Role-based access validation

Prepared statements to prevent SQL injection

Logout invalidates session properly

# 🎓 Academic Relevance

This project demonstrates:

Java Web Technologies

MVC Architecture

JDBC Database Connectivity

Session Management

Role-Based Authorization

## 👩‍💻 Developed By: Team Pinaka
