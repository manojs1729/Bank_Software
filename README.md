Bank Login Application

This project is a Java Swing-based login interface for a hypothetical banking system. It allows users to log in using their credentials stored in a MySQL database and access their account page. New users are prompted to register if they do not already have an account.

Features
User Login: Users can log in with an ID and password.
New User Registration: Prompts the user to register if they do not exist in the database.
Validation and Error Handling: Invalid login attempts are handled with error messages.
UI Theme: Uses the JTattoo HiFi theme for styling.
Project Structure
Main Class
bank: This is the main JFrame class that includes the form UI components and event handling logic for login and registration.

Components
Labels and Text Fields:

jLabel1: Displays a welcome message.
jLabel2 & jTextField1: Label and text field for user ID input.
jLabel3 & jPasswordField1: Label and password field for password input.
jLabel4 & jTextField2: Label and text field for the user's name.
Buttons:

jButton1: "Submit" button that validates login.

jButton2: "New User" button that checks if a user already exists or initiates a new registration.

Database Connection: Connects to a MySQL database (bankpage) to verify user credentials.

Database Configuration
The application connects to a MySQL database using the following parameters:

URL: jdbc:mysql://localhost:3306/bankpage

Username: root

Password: root

Ensure the database bankpage and table userdata exist, with columns id, name, and password to store user credentials.

Getting Started
Prerequisites
Java Development Kit (JDK): Java 8 or above
NetBeans IDE: Recommended for modifying the GUI components.
MySQL Database: Ensure MySQL is installed and running.

Setup

Database Setup:

Create a MySQL database named bankpage.

Create a table named userdata with columns id (VARCHAR), name (VARCHAR), and password (VARCHAR).

Running the Application:

Open the project in NetBeans or any compatible IDE.

Build and run the application.

Enter login credentials (existing user) or register a new user.

Code Overview

Database Query (Login Validation): The application fetches user information using a PreparedStatement to prevent SQL injection attacks.

Event Handling:

jButton1ActionPerformed: Validates the entered ID and password against the database.

jButton2ActionPerformed: Checks if a new user already exists and, if not, opens a registration form (newuser).

UI Theme

The application uses the JTattoo HiFi Look and Feel. Ensure JTattoo library is included in the project dependencies.

Error Handling

Displays error messages for invalid login attempts.
Exception handling for SQL and ClassNotFoundException.
License
This project is provided under an open-source license. You are free to modify and distribute the code as needed.
