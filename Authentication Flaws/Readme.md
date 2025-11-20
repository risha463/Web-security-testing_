DVWA – Authentication Security Testing 

Author: Risha Gupta
Tools Used:

DVWA (Damn Vulnerable Web Application)

XAMPP (Apache + MySQL)

Chrome Developer Tools

1. Overview

This project contains manual authentication-related security tests performed on DVWA.
The objective was to identify weaknesses in:

Login mechanism

Default credentials

Session behavior

Session cookie security

Logout behavior

No automated tools (Burp Suite, OWASP ZAP, etc.) were used.
All tests were done manually using browser and developer tools only.

2. Folder Structure
Authentication_Flaws/
│
├── screenshots/
│   ├── Authentication_Flaws_cookie_test1.png
│   ├── Authentication_Flaws_cookie_test2.png
│   ├── Authentication_Flaws_cookie_test3.png
│   ├── Authentication_Flaws_login_test1.png
│   ├── Authentication_Flaws_login_test2.png
│   ├── Authentication_Flaws_login_test3.png
│   ├── Authentication_Flaws_login_test4.png
│
└── DVWA-Authentication-Report.pdf

3. What Was Tested?
✔ 1. Weak / Default Credentials

DVWA allowed login with admin / password

No password complexity

No lockout

High risk

✔ 2. Manual Login Abuse Check

No rate-limiting

Unlimited login attempts possible

Login brute-force vulnerability confirmed (manual observation)

✔ 3. Broken Session Management

Session ID remained same:

Before login

After login

After logout

Logout didn’t destroy the session

Session Hijacking + Session Fixation possible

✔ 4. Insecure Cookies

Checked manually via:
Developer Tools → Application → Cookies

Findings:

HttpOnly: Disabled

Secure: Disabled

SameSite: Not Set

Session cookie only

This means cookie can be stolen or reused.

4. Report

Full detailed PDF report is available in this repository:
DVWA-Authentication-Report.pdf

5. Purpose of This Project

This project is created to demonstrate:

Manual authentication testing

Understanding login weaknesses

Observing insecure session behavior

Practical cyber security project for portfolio / LinkedIn

6. Disclaimer

This project is for educational purposes only using DVWA (a purposely insecure lab).
Do not run these tests on real websites.
