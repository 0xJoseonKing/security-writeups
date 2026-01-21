# Extracting Data from a Non-Oracle Database via SQL Injection

> ⚠️ This write-up is based on a PortSwigger Web Security Academy lab.  
> All actions were performed in a deliberately vulnerable lab environment for educational purposes only.

## 🎯 Objective
The goal of this lab was to access and display data from a non-Oracle database table containing administrator credentials by exploiting a SQL injection vulnerability.

---

## 🧠 Lab Overview
The application was vulnerable to SQL injection, which made it possible to manipulate the backend SQL query. By leveraging this vulnerability, I was able to enumerate database metadata and identify a table containing sensitive user information, including an administrator username and password.

---

## 🧪 Methodology

### 1️⃣ Determining the Number of Columns
The first step was identifying the number of columns returned by the original SQL query. This was necessary to successfully use a UNION-based SQL injection and ensure the injected query matched the original query structure.

---

### 2️⃣ Identifying a Displayed Column
After determining the correct column count, I tested which column(s) were reflected in the application’s response. This helped identify where extracted data could be displayed on the page.

---

### 3️⃣ Enumerating Database Tables
Using the information_schema.tables view, I enumerated the available tables within the database. Since the lab used a non-Oracle database, this approach allowed me to retrieve table names stored by the database engine.

---

### 4️⃣ Locating the Credentials Table
From the enumerated table names, I identified a table that likely contained user credentials based on naming patterns related to usernames and passwords.

---

### 5️⃣ Extracting Admin Credentials
Once the relevant table was identified, I queried it to retrieve stored usernames and passwords. This revealed the administrator credentials required to complete the lab.

---

## ✅ Outcome
The administrator username and password were successfully extracted from the database and used to solve the lab.

---

## 📚 Key Takeaways
- UNION-based SQL injection requires accurate column enumeration.
- information_schema is critical for database enumeration in non-Oracle systems.
- Table naming conventions often reveal the purpose of stored data.
- Understanding database-specific behaviour improves exploitation efficiency.

---

## 🔒 Ethical Note
This write-up documents a controlled lab exercise from PortSwigger Academy.  
No real-world systems were targeted.
