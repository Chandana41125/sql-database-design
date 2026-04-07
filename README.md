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
