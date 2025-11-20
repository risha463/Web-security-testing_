🔐 DVWA – Reflected XSS Security Testing
Security Testing using OWASP ZAP (Manual + Automated Scan)

Tester: Risha Gupta
Target: DVWA (Localhost, XSS_R Module, Security Level: Low)

📌 Overview

This repository contains manual and automated security testing performed on DVWA’s Reflected XSS module using OWASP ZAP 2.16.

The goal was to:

Identify Reflected Cross‑Site Scripting (XSS)

Capture evidence using OWASP ZAP

Understand how the vulnerability behaves

Document screenshots and steps

🛠 Tools Used

OWASP ZAP 2.16 (HUD Enabled)

Chrome Browser via ZAP Proxy

XAMPP (Apache + MySQL)

DVWA Security Level: Low

🚀 What Was Tested

Module: /vulnerabilities/xss_r/
Testing Performed:

Manual payload injection

HTML reflection analysis

Browser behavior checking

ZAP HUD observation

Spider + Active Scan

🧪 Payloads Used
"><script>alert(1)</script>

"><img src=x onerror=alert('XSS')>

"><svg onload=alert('XSS')>

✅ Result (Summary)

✔ Reflected XSS Confirmed
✔ Input not sanitized
✔ Payload reflected in HTML
✔ ZAP Active Scan triggered High‑risk XSS alert

📸 Manual Test Screenshots
![Manual Test 1](XSS_manual_test1.png)
![Manual Test 2](XSS_manual_test2.png)
![Manual Test 3](XSS_manual_test3.png)
![Manual Test 4](XSS_manual_test4.png)

📸 Automated Test Screenshots (OWASP ZAP)
![Automated Test 1](XSS_automated_test1.png)
![Automated Test 2](XSS_automated_test2.png)
![Automated Test 3](XSS_automated_test3.png)
![Automated Test 4](XSS_automated_test4.png)

🔍 Proof of Concept (PoC) URL
http://localhost/dvwa/vulnerabilities/xss_r/?name=%22%3E%3Cscript%3Ealert(1)%3C/script%3E

🛡 Fix Recommendations

Apply output encoding

Validate and sanitize user input

Implement Content Security Policy (CSP)

Avoid printing raw user input

Use frameworks with built‑in escaping

📁 Repository Contains

Manual XSS testing screenshots

Automated (ZAP Active Scan) screenshots

README summary

Evidence of the vulnerability

✨ Author

Risha Gupta
