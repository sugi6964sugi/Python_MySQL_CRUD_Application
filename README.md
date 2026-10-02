Python MySQL CRUD Application
📌 Project Description

This is a Python-based MySQL CRUD Application that allows users to manage records through a simple command-line interface.

The application performs four major database operations:

Insert records
Select records
Update records
Delete records

The project uses MySQL as the database and Python for application development.

🛠️ Technologies Used
Python
MySQL
MySQL Connector/Python
Tabulate
📦 Python Libraries

The following Python libraries are required:

pip install mysql-connector-python
pip install tabulate

Or install both at once:

pip install mysql-connector-python tabulate
🗄️ Database Setup

First, create a database in MySQL:

CREATE DATABASE data;

Select the database:

USE data;

Create the required table:

CREATE TABLE data (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    age INT,
    address VARCHAR(255),
    contact VARCHAR(20),
    mail VARCHAR(100)
);
🔗 MySQL Connection

The Python program connects to MySQL using mysql.connector.

Use your own MySQL password:

con = mysql.connector.connect(
    host="localhost",
    user="root",
    password="YOUR_PASSWORD",
    database="data"
)
⚠️ Security Note

Do not upload your real MySQL password to GitHub.

Replace:

password="YOUR_PASSWORD"

with your password only on your local machine.

✨ Features
1. Insert Record

The insert() function collects:

Name
Age
Address
Contact
Mail

and inserts the information into the MySQL table.

def insert():
2. Select Records

The select() function retrieves all records from the database using:

SELECT * FROM data;

The tabulate library is used to display the records in a formatted table.

Example:

+----+---------+-----+------------+------------+-------------------+
| ID | NAME    | AGE | ADDRESS    | CONTACT    | MAIL              |
+----+---------+-----+------------+------------+-------------------+
|  1 | Sugima  |  22  | Coimbatore | 9876543210 | example@gmail.com |
+----+---------+-----+------------+------------+-------------------+
3. Update Record

The update() function allows the user to update individual fields.

Available options:

1. Name
2. Age
3. Address
4. Contact
5. Mail

The record is updated using its ID.

For example:

UPDATE data
SET name=%s
WHERE id=%s;
4. Delete Record

The delete() function removes a record from the database using its ID.

DELETE FROM data
WHERE id=%s;
🔄 CRUD Operations
Operation	SQL Command	Python Function
Create	INSERT	insert()
Read	SELECT	select()
Update	UPDATE	update()
Delete	DELETE	delete()
📋 Application Menu

When the program runs, the following menu is displayed:

1.Insert Record
2.Select Record
3.Update Record
4.Delete Record
5.Exit

Enter Your Choice :
Menu Options

1 - Insert Record
Adds a new record to the database.

2 - Select Record
Displays all existing records.

3 - Update Record
Updates a selected field using the record ID.

4 - Delete Record
Deletes a record using its ID.

5 - Exit
Closes the application.

▶️ How to Run the Project
Step 1: Install Python

Check whether Python is installed:

python --version
Step 2: Install Required Libraries
pip install mysql-connector-python tabulate
Step 3: Start MySQL

Make sure your MySQL server is running.

Step 4: Create Database and Table

Run the SQL commands given in the Database Setup section.

Step 5: Configure MySQL Connection

Update your MySQL username, password, and database name in the Python file.

Step 6: Run the Python Program
python main.py
📂 Project Structure
Python-MySQL-CRUD/
│
├── main.py
├── README.md
└── requirements.txt
📄 requirements.txt

Create a file named requirements.txt and add:

mysql-connector-python
tabulate

Then install all dependencies using:

pip install -r requirements.txt
🧠 Concepts Used

This project demonstrates the following concepts:

Python functions
User input
Conditional statements
While loop
MySQL connectivity
SQL queries
Database cursor
commit()
fetchall()
Parameterized SQL queries
CRUD operations
Tabular data display
🚀 Future Enhancements

The project can be improved by adding:

Input validation
Exception handling
Search functionality
Login authentication
Contact number validation
Email validation
Better error messages
GUI using Tkinter
Web application using Flask
Environment variables for database credentials
🎯 Learning Objective

The main objective of this project is to understand how Python communicates with a MySQL database and how CRUD operations can be implemented using SQL queries.

This project is suitable as a beginner-level Python and MySQL project for learning and portfolio purposes.

