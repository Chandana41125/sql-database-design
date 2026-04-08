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