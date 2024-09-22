
# CRUD Form Application design using C# language.



## Project Overview
This is a simple CRUD form where you can insert, update, delete and search your inputed data. And also you can see your inputed data on this crudform from data grid view table.
## Technologies Used
C#: Core programming language

.NET Framework/Core: Application framework

Entity Framework: ORM for database access

SQL Server or SQLite: Database (choose one based on my project)

Visual Studio: IDE for development

### Prerequisites:

Visual Studio 2022 or later

SQL Server (Express or any version)

SQL Server Management Studio 2022 (SSMS)
## key Features
Insert new People: Users can insert People details such as ID, Name, and Age. When the "Insert" button is clicked, the new People is added to the list and the database.

Update Information: Users can select an existing id from the grid and update their details using the "Update" button. This will modify the selected id information in the database.

Delete Records: Select a id from the grid and click the "Delete" button to remove their record from the system. A confirmation can be implemented to avoid accidental deletions.


Search ID: Users can search for a ID by ID, Name, or Age using the "Search" button, and the grid will update to show only the relevant records.


View/Search Information: The application displays all records in a grid format, showing the ID, name, and age.

#### Schema Diagram:
<img width="451" alt="1" src="https://github.com/user-attachments/assets/a125e32b-5008-4570-b1f3-7fecdb1cf5a2">

## Set Up SQL Server Database:
Open SQL Server Management Studio (SSMS) and connect to your SQL Server instance.

Create the Database:

Open the .sql file located in folder.
Copy the queries from the .sql file and execute them in your new database to set up the schema and initial data.

#### Use Ctrl+F to search for connectionString within the project files.
SqlConnection con = new SqlConnection("Data Source=RAKIB\\SQLEXPRESS;Initial Catalog=CURDFormApp;Integrated Security=True;Encrypt=False");

#### Update this to:
private readonly string connectionString = ("Data Source=RAKIB\\SQLEXPRESS;Initial Catalog=CURDFormApp;Integrated Security=True;Encrypt=False");

#### Create a Table for Student Information:

CREATE TABLE Students (

StudentId INT PRIMARY KEY IDENTITY(1,1),
Name NVARCHAR(100) NOT NULL,
Age INT NOT NULL
); GO

This table will store StudentId, Name, and Age.

Create a C# Windows Forms Application:

Open Visual Studio.
Create a New Project:

Select C# > Windows Forms App (.NET Framework).
Choose a project name and location.
Design Your Form:

Add text boxes for StudentId, Name, and Age.
Add buttons for Insert, Update, Delete, and Search.
Add a DataGridView to display student records.
Add SQL Server Connection: To connect your application to the SQL Server database, you need to configure a connection string.

Install SQL Server NuGet Package (optional if not already available):

In Solution Explorer, right-click on the project and select Manage NuGet Packages.
Search for System.Data.SqlClient and install it.
Set up the Connection String in your C# code: In your code-behind file (e.g., Form1.cs), define the connection string:

string connectionString = "Data Source=YOUR_SERVER_NAME;Initial Catalog=StudentDB;Integrated Security=True;";
Replace (YOUR_SERVER_NAME) with the actual name of your SQL Server (you can find this in SSMS).
## Code Implementation:
#### Insert data function sample:
<img width="698" alt="2" src="https://github.com/user-attachments/assets/d18346be-6669-484b-b47c-35b9be2e695e">
#### Update data function sample:
<img width="698" alt="3" src="https://github.com/user-attachments/assets/747f97f0-ec92-49ff-b220-a3d4e1307b97">
#### Delete Operation:
<img width="701" alt="4" src="https://github.com/user-attachments/assets/ecb5f1df-6c31-4b24-ba98-25af435ec8f5">
#### Search Operation:
<img width="701" alt="5" src="https://github.com/user-attachments/assets/33b56a5f-c86a-4c2a-b01c-f839542e689a">

## Screenshots
<img width="645" alt="6" src="https://github.com/user-attachments/assets/cf1ff629-8eb0-4d3c-b5ae-ef9f2223f2db">


## Event Handling
mplement event handlers for each button (e.g., Create, Edit, Delete).
When a button is clicked, the corresponding CRUD operation will be executed (e.g., creating a new record or deleting an existing one).
## Build and Run the Application:
Open the project in Visual Studio, build it, and run the application.
## How to Run the Project
Clone the Repository: Clone this repository to your local machine.
git clone https://github.com/Sadikuzzamanrakib/CRUDForm

Set Up the Database: Configure your SQL Server or SQLite database and update the connection according to the script.sql file.

Build the Project: Open the project in Visual Studio and build the solution.

Run the Application: Once built, run the application and manage records through the Windows Forms interface.
