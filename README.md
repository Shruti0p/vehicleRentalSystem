Vehicle Rental Management System (ASP.NET Core & MySQL)

Description

This is a full-stack web application built using ASP.NET Core MVC (C#) designed to manage a fleet of rental vehicles and their associated bookings.

The project implements robust CRUD operations across two related entities: Vehicles and Rentals. Crucial business logic and validation are enforced to ensure data integrity for vehicle availability, booking, and returns.

Key Features:

Technology Stack: ASP.NET Core MVC (C#), Entity Framework Core (Code-First), MySQL/MariaDB (used via XAMPP), and Tailwind CSS for a professional, responsive frontend.

Status Management: Automatic updating of a Vehicle's Status (Available, Rented, Maintenance) based on booking and return actions.

Validation: Prevents actions like deleting a vehicle or editing core details while the vehicle is currently rented.

Dashboard: Provides a real-time summary of the current fleet status.

🛠️ Installation & Database Setup

This project uses Entity Framework Core with the Pomelo provider to connect to a MySQL database, typically run through XAMPP.

Prerequisites

.NET SDK (v9.0 or later): Used to build and run the ASP.NET Core application.

MySQL/MariaDB: The database server (Ensure XAMPP MySQL service is running).

1. Configure Project and Packages

Navigate to your project root directory (C:\Users\patel\Desktop\5th Sem\net\Project\Shruti\RentalSystem) in the terminal:

# 1. Restore project dependencies
dotnet restore

# 2. Rebuild the solution to ensure all files are compiled
dotnet build


2. Apply Database Migrations

Ensure your appsettings.json file contains the correct connection string for your XAMPP MySQL setup (Server=localhost;Port=3306;Database=RentalSystemDb;Uid=root;Pwd=;).

# 1. Create the initial migration files (if needed)
dotnet ef migrations add InitialCreate

# 2. Apply the migration to your MySQL database (RentalSystemDb)
dotnet ef database update


How to Run the Project

Start the Web Server: Run the application using the following command:

dotnet run


Access the Website: The console output will display the listening URLs. Copy the HTTPS address (e.g., https://localhost:7001) and paste it into your web browser.

The application will launch to the Dashboard page, where you can begin adding vehicles and testing the rental functionality.
