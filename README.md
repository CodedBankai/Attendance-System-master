This attendance management project is a web-based system designed to help teachers track student attendance. Based on the PHP files provided, the system offers comprehensive functionality for managing classes, recording attendance, and generating attendance reports.

Core Functionality

 User Authentication System
 The project implements a secure login and registration system for teachers. It uses blowfish hashing algorithm for password security, with functions like hashPass() and verifyPass() to handle password encryption and verification. Teachers can sign up with their name, 
 email, phone, and password, and then log in using their credentials.

Class Management
 Teachers can create, update, and delete classes they teach. Each class is represented by:

 Subject code (following a specific format like "XXX-123")

 Section number

 Year

 Semester

 Roll number range (start and end)

 The system allows teachers to update class details such as section, year, semester, and subject code. They can also delete classes they no longer teach.

Attendance Tracking
 The core functionality revolves around marking and tracking student attendance:

 Teachers can mark attendance for students in their classes

 The system records timestamps for each attendance entry

 It maintains a timeline of attendance for each student

 It calculates attendance percentages automatically

Roll Number Management
 The system supports adding and removing students (by roll number) from classes. Roll numbers follow a specific format (e.g., "123/XX/22") which is validated using regex patterns. Teachers can delete roll numbers from their classes when needed.

 Technical Implementation
 Database Structure
 The system uses a MySQL database with at least two main tables:

 teacher: Stores teacher information (name, email, phone, password)

 objects: Stores class information with serialized PHP objects

Object-Oriented Approach
 The project uses an object-oriented design with a Node class that represents classes and their attendance records. This class provides methods for:

 Initializing records for a range of roll numbers

 Setting and getting attendance data

 Calculating attendance percentages

 Managing timelines of student attendance

Security Features
 The code implements several security measures:

 Password hashing using blowfish algorithm

 SQL injection prevention through mysqli_real_escape_string()

 Input validation using regular expressions

 Session management for authenticated users

Data Retrieval and Reporting
 The system can generate attendance reports showing:

 Timeline of a student's attendance

 Attendance percentage

 Total number of classes conducted

 Teacher information

The project follows a modular approach with separate PHP files handling different functionalities, making it maintainable and extensible. It uses JSON for data exchange between the server and client, suggesting it has a frontend component that interacts with these PHP backend scripts.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

I have used VS code to run the project so i had to use the PHP debuger and XAMPP software.
You can just use XAMPP its enough as it has inbuid PHP.
