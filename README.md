🏥 Hospital Management System (Java CLI + MySQL)

A Command Line Interface (CLI) based Hospital Management System built using Java and MySQL. This project allows basic hospital operations such as managing patients, viewing doctors, and booking appointments.

📌 Features
🧑 Add Patient
📋 View Patients
👨‍⚕️ View Doctors
📅 Book Appointment

🛠️ Tech Stack
Language: Java (JDK 8 or higher)
Database: MySQL
Connectivity: JDBC (MySQL Connector/J)
Interface: Command Line (CLI)

📂 Project Structure
Hospital-Management-System/
│── src/
│   ├── Main.java
│   ├── DBConnection.java
│   ├── Patient.java
│   ├── Doctor.java
│   ├── Appointment.java
│
│── database/
│   └── schema.sql
│
│── lib/
│   └── mysql-connector-j.jar
│
│── README.md

⚙️ Installation & Setup
1️⃣ Clone the Repository
git clone https://github.com/farahan-nadaf/hospital-management-system.git
cd hospital-management-system

2️⃣ Setup MySQL Database
CREATE DATABASE hospital_db;
Import schema:
mysql -u root -p hospital_db < database/schema.sql

3️⃣ Configure Database Connection

Edit DBConnection.java:
String url = "jdbc:mysql://localhost:3306/hospital_db";
String user = "root";
String password = "your_password";

4️⃣ Compile and Run
Compile:
javac -cp ".;lib/mysql-connector-j.jar" src/*.java
Run:
java -cp ".;lib/mysql-connector-j.jar;src" Main
💡 On Linux/Mac, replace ; with :

🧑‍💻 Usage

When you run the program, you will see:

===== Hospital Management System =====
1. Add Patient
2. View Patients
3. View Doctors
4. Book Appointment
5. Exit
Enter your choice
Follow the prompts

🗄️ Database Tables
Patients
Doctors
Appointments
Example Table
CREATE TABLE patients (
    patient_id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    age INT,
    gender VARCHAR(10)
);

🚀 Future Improvements
Update & Delete Patient Records
Billing System
GUI Interface (JavaFX/Swing)
Login Authentication

📜 License
This project is licensed under the MIT License.
