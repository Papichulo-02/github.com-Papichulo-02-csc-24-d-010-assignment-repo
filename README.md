
# NAME: IDOGWU ADOYI ABRAHAM 
# MATRIC NUMBER: 24/D/CSC/010
# COURSE CODE: CSC 282
# COURSE TITLE: COMPUTER LAB I
# ASSIGNMENT TITLE: STUDENT REGISTRATION SYSTEM
Create a PHP web application for registering students. Requirements • A form with fields: o Full Name o Email o Department o Matric Number • A PHP script (process.php) that: o Validates inputs (all fields required, email must be valid). o Saves the data into a MySQL database (student_records table). • A view.php page that displays all registered students in a table.

This is a simple PHP web application for registering students. It allows users to input student details and stores them in a MySQL database. The application also provides functionality to view all registered students and delete records as needed.

# Project Structure
student-registration-app
│   ├── config
│   │   └── db.php          # Database connection settings
│   ├── process.php         # Handles form submission and data validation
│   ├── view.php            # Displays all registered students
│   ├── delete.php          # Processes deletion of student records
│   └── index.php           # Landing page with registration form
# Setup Instructions
1. Clone the repository:

git clone <repository-url>
cd student-registration-app
2. Create a MySQL database: Create a database named student_registration and a table named student_records with the following structure:

CREATE TABLE student_records (
    id INT AUTO_INCREMENT PRIMARY KEY,
    full_name VARCHAR(100) NOT NULL,
    email VARCHAR(100) NOT NULL,
    department VARCHAR(100) NOT NULL,
    matric_number VARCHAR(50) NOT NULL
);
3. Configure the database connection: Edit the db.php file to include your database credentials:

<?php
$host = 'localhost';
$db   = 'student_registration';
$user = 'your_username';
$pass = 'your_password';
$charset = 'utf8mb4';

$conn = new mysqli($host, $user, $pass, $dbname);

if ($conn->connect_error) {
 die("Connection failed: " . $conn->connect_error);
}
?>
4. Run the application: Open index.php in your web browser to access the registration form. Fill in the details and submit to register a student.

# Additional Information
Ensure that your server has PHP and MySQL installed.
