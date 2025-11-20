🔐 Web Application Security Testing – DVWA
Author: Risha Gupta

This repository contains three complete DVWA security testing projects:
1️⃣ SQL Injection
2️⃣ Authentication Security Testing
3️⃣ Reflected XSS (Cross‑Site Scripting)

All tests were performed on DVWA running on XAMPP, using manual and automated techniques.

📁 Repository Structure
DVWA-Security-Testing/
│
├── SQL_Injection/
│   ├── screenshots/
│   └── DVWA_SQL_Injection_Report.pdf
│
├── Authentication_Flaws/
│   ├── screenshots/
│   └── DVWA-Authentication-Report.pdf
│
├── XSS_Reflected/
│   ├── screenshots/
│   └── DVWA_XSS_Report.pdf
│
└── README.md

🛠 Tools Used

DVWA

XAMPP (Apache + MySQL)

Chrome Developer Tools

OWASP ZAP 2.16

SQLMap

🌐 TASK 1 – Web Application Security Testing

Goal: Identify vulnerabilities including:
✔ SQL Injection
✔ XSS
✔ Authentication flaws
✔ Session management issues

Deliverables: Security reports + screenshots.

🔥 1. SQL Injection Testing
✔ Overview

Performed manual SQL Injection + SQLMap automated exploitation.

✔ Key Activities

User ID injection

Authentication bypass

Database extraction using SQLMap

Dumped users table

✔ Findings

SQL Injection confirmed

DB fully compromised

Sensitive user data exposed

✔ Recommendations

Use prepared statements

Validate & sanitize input

Remove detailed SQL errors

📸 Screenshots

(Stored in: SQL_Injection/screenshots/)

🔥 2. Authentication Security Testing
✔ Overview

Manual authentication and session testing using Chrome DevTools.

✔ What Was Tested
1. Weak Credentials

Login allowed: admin / password

No password policy

No account lockout

2. Login Abuse

Unlimited attempts

Brute-force possible

3. Broken Session Management

Same session ID before + after login

Logout did not invalidate session

4. Insecure Cookies

HttpOnly: OFF

Secure: OFF

SameSite: Missing

📸 Screenshots

(Stored in: Authentication_Flaws/screenshots/)

🔥 3. Reflected Cross-Site Scripting (XSS) Testing
✔ Overview

Tested DVWA’s Reflected XSS module manually + via OWASP ZAP.

✔ Payloads Used

"><script>alert(1)</script>

"><img src=x onerror=alert('XSS')>

"><svg onload=alert('XSS')>

✔ Findings

Input reflected without sanitization

Script executed

ZAP detected High‑risk XSS

Parameter: name vulnerable

✔ Recommendations

HTML encoding (escape special chars)

Input validation

Add CSP header

Avoid returning raw user input

📸 Screenshots

(Stored in: XSS_Reflected/screenshots/)

📄 Reports Included

SQL Injection Report

Authentication Security Testing Report

Reflected XSS Security Testing Report

(Each report is inside its respective project folder.)

🎯 Purpose

This repository demonstrates:

Practical web application penetration testing

Understanding vulnerabilities deeply

Creating portfolio‑ready cybersecurity work

⚠ Disclaimer

This project uses DVWA, a purposely vulnerable lab.
Do NOT test these techniques on real websites.

👩‍💻 Author
Risha Gupta

Web Application Security | Ethical Hacking Learner
