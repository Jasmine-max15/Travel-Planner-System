The Travel Planner System is a simple command-line application developed using Python and MySQL.
It allows users to manage travel information by storing users, destinations, hotels, and trips in a database.

The project demonstrates how Python interacts with a MySQL database to perform operations like inserting, retrieving, and managing data.

This system helps in planning trips by selecting a destination, hotel, travel dates, and budget.

Technologies Used
Python
MySQL
mysql.connector (Python Library)
SQL
Project Features
1. Add User

Allows adding a new user to the system.

Information stored:

User Name
Email
2. Add Destination

Stores travel destinations.

Information stored:

City
Country
3. Add Hotel

Stores hotel details for a destination.

Information stored:

Hotel Name
City
Price per night
4. Plan Trip

Allows a user to plan a trip by selecting:

User ID
Destination ID
Hotel ID
Start Date
End Date
Budget
5. View Trips

Displays all planned trips by combining data from multiple tables using SQL JOIN queries.

Displayed information:

User name
Destination
Hotel
Travel dates
Budget
Database Structure
Database Name
travel_planner

Tables
Users
Column	Type	Description
user_id	INT	Primary Key
name	VARCHAR	User name
email	VARCHAR	User email
Destinations
Column	Type	Description
destination_id	INT	Primary Key
city	VARCHAR	Destination city
country	VARCHAR	Destination country
Hotels
Column	Type	Description
hotel_id	INT	Primary Key
name	VARCHAR	Hotel name
city	VARCHAR	Hotel city
price_per_night	INT	Hotel price
Trips
Column	Type	Description
trip_id	INT	Primary Key
user_id	INT	Foreign key
destination_id	INT	Foreign key
hotel_id	INT	Foreign key
start_date	DATE	Trip start
end_date	DATE	Trip end
budget	INT	Trip budget
SQL Setup

Example SQL for creating a simple student table (practice database):

CREATE DATABASE college;
USE college;

CREATE TABLE students (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    course VARCHAR(50)
);

INSERT INTO students VALUES (1,'Himanshu','MCA');
INSERT INTO students VALUES (2,'Rahul','BCA');
INSERT INTO students VALUES (3,'Anushree','MBA');
INSERT INTO students VALUES (4,'Kanishka','BCA');
INSERT INTO students VALUES (5,'Tanuja','BCA');
Python Program

The Python script connects to the MySQL database and provides a menu-driven system.

Menu options:

Travel Planner
1 Add User
2 Add Destination
3 Add Hotel
4 Plan Trip
5 View Trips
6 Exit

The program performs database operations using SQL queries through Python.

How to Run the Project
Step 1

Install MySQL and create the required database.

Step 2

Install the MySQL connector library in Python.

pip install mysql-connector-python
Step 3

Update database credentials in the Python file.

host="localhost"
user="root"
password="your_password"
database="travel_planner"
Step 4

Run the Python program.

python travel_planner.py
Learning Outcomes

This project helps understand:

Python database connectivity
SQL database operations
Table relationships
CRUD operations
Menu-driven Python programs
