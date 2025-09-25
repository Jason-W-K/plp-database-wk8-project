# ClinicDB Database

This project defines a relational database schema for managing a clinic system.  
It includes patients, doctors, their specializations, appointments, and treatments.

---

## Database Setup

Run the following SQL commands to create the database and tables:

```sql
-- Create the database
CREATE DATABASE ClinicDB;
USE ClinicDB;

-- Create Patients table
CREATE TABLE Patients (
    PatientID INT AUTO_INCREMENT PRIMARY KEY,
    FirstName VARCHAR(50) NOT NULL,
    LastName VARCHAR(50) NOT NULL,
    DOB DATE NOT NULL,
    Gender ENUM('Male', 'Female', 'Other') NOT NULL,
    Phone VARCHAR(15) UNIQUE,
    Email VARCHAR(100) UNIQUE
);

-- Create Doctors table
CREATE TABLE Doctors (
    DoctorID INT AUTO_INCREMENT PRIMARY KEY,
    FirstName VARCHAR(50) NOT NULL,
    LastName VARCHAR(50) NOT NULL,
    Email VARCHAR(100) UNIQUE,
    Phone VARCHAR(15) UNIQUE
);

-- C
