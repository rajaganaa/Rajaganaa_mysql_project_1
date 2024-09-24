# Project Name: rajaganaa_mysql_project

Description: This project demonstrates the creation and management of a MySQL database for a university system, including student, course, instructor, and enrollment data. It includes sample data for each table and showcases various SQL queries to retrieve, analyze, and manipulate the information.

# Database Structure:

# STUDENT:
studentId (INT PRIMARY KEY AUTO_INCREMENT)
firstName (VARCHAR(50) NOT NULL)
lastName (VARCHAR(50) NOT NULL)
email (VARCHAR(100) NOT NULL UNIQUE)
course (VARCHAR(50))
yearOfJoining (INT)
# COURSE:
courseId (INT PRIMARY KEY AUTO_INCREMENT)
courseName (VARCHAR(100) NOT NULL)
branches (VARCHAR(50))
courseFees DECIMAL(10,2) NOT NULL
# INSTRUCTOR:
instructorId (INT PRIMARY KEY AUTO_INCREMENT)
firstName (VARCHAR(50) NOT NULL)
lastName (VARCHAR(50) NOT NULL)
email (VARCHAR(100) NOT NULL UNIQUE)
branches (VARCHAR(50))
# ENROLLMENT:
enrollmentId (INT PRIMARY KEY AUTO_INCREMENT)
studentId (INT NOT NULL, FOREIGN KEY (studentId) REFERENCES STUDENT(studentId))
courseId (INT NOT NULL, FOREIGN KEY (courseId) REFERENCES COURSE(courseId))
enrollmentDate (DATE NOT NULL)
# Sample Data:

This project includes sample data inserted into each table for demonstration purposes.

# SQL Queries:

The project showcases various SQL queries for data retrieval and analysis, including:

Basic SELECT statements: Retrieving all data from a table.
JOIN operations: Combining data from multiple tables.
Filtering: Selecting data based on specific criteria.
Aggregation functions: Calculating totals, counts, averages, etc.
Ordering and ranking: Sorting data based on criteria.
Identifying specific information: Finding courses a student is not enrolled in.
Combining related data: Combining student information with enrolled courses and fees.
