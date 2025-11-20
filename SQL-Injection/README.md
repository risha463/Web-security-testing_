# DVWA SQL Injection Security Testing Project

## 📌 Overview
This project demonstrates **SQL Injection vulnerability testing** performed on  
**DVWA (Damn Vulnerable Web Application)** running on a local XAMPP server.

The goal of this project:
- Understand how SQL Injection works  
- Perform manual SQLi exploitation  
- Automate SQL Injection using SQLMap  
- Extract database information  
- Dump user credentials  
- Learn the security impact and how to fix SQLi  

This project is created by **Risha Gupta** for learning & practice.


---

## 📁 Project Structure

SQL-Injection/
│
├── report/
│ └── DVWA_SQL_Injection_Report.pdf
│
├── screenshots/
│ ├── sql_manual1.png
│ ├── sql_manual2.png
│ ├── sql_manual3.png
│ ├── sqlmap1.png
│ ├── sqlmap2.png
│ ├── sqlmap3.png
│ ├── sqlmap4.png
│ ├── sqlmap5.png
│ ├── sqlmap6.png
│ └── sqlmap7.png
│
└── README.md

yaml
Copy code

**screenshots folder →** All manual + SQLMap evidence  
**report folder →** Final PDF report  
**README.md →** Project summary


---

## 🛠 Tools Used
- **DVWA**
- **XAMPP** (Apache + MySQL)
- **Browser DevTools (Chrome)**
- **SQLMap (for automated SQL Injection)**  
*(No BurpSuite used in this testing)*

---

## 🚀 What Was Tested

### ✔ Manual SQL Injection
- Tested user ID field
- Broke SQL query using `'`
- Extracted all users using `' OR '1'='1`

### ✔ Login Bypass
- Used SQLi payload to bypass authentication

### ✔ SQLMap Automation
- Detected SQLi
- Extracted all database names
- Listed DVWA tables
- Dumped **users** table
- Recovered hashed passwords

---

## 🔍 Key Findings
- SQL Injection confirmed (manual + automated)
- Full database exposure
- User credentials leaked
- Application completely compromised

---

## 🔐 How to Fix SQL Injection
- Use parameterized queries  
- Validate all user input  
- Disable verbose SQL error messages  
- Apply least-privilege principle  
- Use strong password hashing

---

## 📄 Report
Full detailed report is available here:  
📁 `report/DVWA_SQL_Injection_Report.pdf`

---

## 👩‍💻 Author
**Risha Gupta**  
SQL Injection & Web Security Practice Project (DVWA)

---

## ⚠️ Disclaimer
This project is ONLY for educational and ethical learning purposes.  
Do NOT test these techniques on real websites.
