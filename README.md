# 📊 Student & Branch Database Schema (MySQL)

## 📌 Overview
This project contains SQL scripts to create a structured database for managing:
- Student details
- Branch information

It demonstrates the use of constraints like:
- Primary Key
- Unique Key
- Check Constraints

---

## 🗂️ Database Name
CHOMBU

---

## 🧱 Tables

### 👨‍🎓 STUDENT Table
| Column | Type | Constraints |
|--------|------|------------|
| SID | INT | Primary Key |
| SNAME | VARCHAR(20) | NOT NULL |
| PHONE | BIGINT | UNIQUE, NOT NULL, CHECK (10 digits) |

---

### 🏢 BRANCH Table
| Column | Type | Constraints |
|--------|------|------------|
| BID | INT | Primary Key |
| BNAME | VARCHAR(20) | NOT NULL |
| ADDRESS | VARCHAR(30) | NOT NULL |
| PINCODE | INT | UNIQUE, CHECK (6 digits) |

---

## ⚙️ Features
- Data integrity using constraints
- Unique validation for phone number and pincode
- Clean relational schema design

---

## 🛠️ Technologies Used
- MySQL

---

## 🚀 How to Run
1. Open MySQL Workbench
2. Run the SQL script:
   ```sql
   SOURCE student_branch_schema.sql;


# 🗄️ MySQL Practice - Table Design

This repository contains SQL table creation scripts for practicing database design using MySQL.

---

## 📌 Tables Included

### 🔹 PRODUCT
- Stores product details
- Constraints:
  - Primary Key on PID
  - Price must be greater than 0
  - Quantity must be greater than 0

---

### 🔹 FACULTY
- Stores faculty details
- Constraints:
  - Primary Key on FID
  - Unique phone number
  - Phone must be exactly 10 digits

---

### 🔹 CUSTOMER
- Stores customer information
- Constraints:
  - Auto Increment Primary Key (CID)
  - Unique phone number
  - Default balance is 10
  - Gender restricted using ENUM
  - Foreign key (SID) references STUDENT table

---

## ⚙️ Features
- Use of PRIMARY KEY, UNIQUE, CHECK constraints
- Use of ENUM and DEFAULT values
- Foreign key relationship implementation

---

## 🚀 How to Run

1. Open MySQL Command Line or Workbench
2. Select your database:
   ```sql
   USE your_database_name;

   # 🌍 Tour Data Management System (MySQL)

This project contains SQL scripts to create a relational database for managing tour bookings.

---

## 📌 Database Name
TOUR_DATA

---

## 🧩 Tables Overview

### 🔹 CUSTOMER
Stores customer details.
- Primary Key: CUSTOMER_ID

---

### 🔹 DESTINATION
Stores travel destination details.
- Primary Key: DESTINATION_ID

---

### 🔹 PACKAGES
Stores tour package details.
- Primary Key: PACKAGE_ID
- Foreign Key:
  - DESTINATION_ID → DESTINATION

---

### 🔹 BOOKINGS
Stores booking records.
- Primary Key: BOOKING_ID
- Foreign Keys:
  - CUSTOMER_ID → CUSTOMER
  - PACKAGE_ID → PACKAGES

---

## 🔗 Relationships

- One CUSTOMER can have multiple BOOKINGS
- One PACKAGE can be booked multiple times
- Each PACKAGE belongs to one DESTINATION

---

## ⚙️ Features

- Use of PRIMARY KEY and FOREIGN KEY constraints
- ENUM used for booking status
- Relational database design

---

## 🚀 How to Run

1. Open MySQL Workbench or Command Line
2. Run:
   ```sql
   SOURCE database.sql;
   SOURCE customer.sql;
   SOURCE destination.sql;
   SOURCE packages.sql;
   SOURCE bookings.sql;



# 🏥 Hospital Management System (MySQL)

This project contains SQL scripts to create a relational database for managing hospital operations.

---

## 📌 Database Name
HOSPITAL

---

## 🧩 Tables Overview

### 🔹 DOCTORS
Stores doctor details.
- Primary Key: DOC_ID

---

### 🔹 PATIENTS
Stores patient details.
- Primary Key: PAT_ID

---

### 🔹 MEDICATION
Stores prescribed medicines.
- Primary Key: MED_ID
- Foreign Keys:
  - PAT_ID → PATIENTS
  - DOC_ID → DOCTORS

---

### 🔹 APPOINTMENTS
Stores appointment details.
- Primary Key: APP_ID
- Foreign Keys:
  - DOC_ID → DOCTORS
  - PAT_ID → PATIENTS

---

### 🔹 BILLS
Stores billing information.
- Primary Key: BILL_ID
- Foreign Key:
  - APP_ID → APPOINTMENTS

---

## 🔗 Relationships

- One DOCTOR can treat many PATIENTS
- One PATIENT can have multiple APPOINTMENTS
- MEDICATION links DOCTOR and PATIENT
- Each APPOINTMENT can generate one BILL

---

## ⚙️ Features

- Use of PRIMARY KEY and FOREIGN KEY constraints
- ENUM used for status tracking
- Real-world relational database design

---

## 🚀 How to Run

1. Open MySQL Workbench or Command Line
2. Execute in order:
   ```sql
   SOURCE database.sql;
   SOURCE doctors.sql;
   SOURCE patients.sql;
   SOURCE medication.sql;
   SOURCE appointments.sql;
   SOURCE bills.sql;