# PortSwigger Labs

![portswigger screenshot](./screenshots/portswigger-dashboard.png) 

## Authentication

### a) Username Enumeration via Different Responses (Brute Force Attack)
Initially, I encountered technical difficulties setting up Burp Suite on my Intel-based Mac, which delayed my progress. However, once resolved, I was able to apply foundational knowledge of HTTP methods, particularly POST and GET, to navigate the lab effectively. This exercise deepened my understanding of how inconsistent server responses can inadvertently reveal valid usernames, making brute-force attacks more feasible.

### b) Username Enumeration via Subtly Different Responses
This lab emphasized the importance of subtle variations in error messages during authentication attempts. By leveraging Burp Suite’s Grep - Extract feature, I was able to isolate and compare response messages, ultimately identifying a valid username based on a minor textual discrepancy. The challenge reinforced the value of precision in analyzing server behavior and the risks posed by inconsistent feedback mechanisms.

## SQL Injection

### a) SQL Injection in WHERE Clause (Retrieving Hidden Data)
This lab demonstrated how vulnerable SQL queries can be manipulated to bypass logical conditions. By injecting '+OR+1=1-- into the category filter, I successfully retrieved unreleased products. The exercise clarified how improper input sanitization can expose sensitive data and underscored the importance of secure query construction.

### b) SQL Injection Allowing Login Bypass
Through this lab, I explored how SQL injection can compromise authentication systems. By crafting a payload that manipulated the login query, I was able to bypass credential checks and gain unauthorized access. This reinforced the critical need for parameterized queries and robust input validation in login mechanisms.

## Access Control

### a) Unprotected Admin Functionality
In this lab, I discovered an exposed administrative endpoint by accessing /robots.txt, which revealed a Disallowdirective pointing to /administrator-panel. Navigating to this path granted access to the admin interface, where I successfully deleted the user carlos. The exercise highlighted how misconfigured access controls and publicly disclosed paths can lead to privilege escalation.

### b) Unprotected Admin Functionality with Unpredictable URL
This scenario required deeper inspection of the application’s source code. By reviewing embedded JavaScript, I identified the hidden admin panel URL and accessed it directly. The lab emphasized the importance of obfuscating sensitive endpoints and avoiding client-side disclosure of administrative paths.


# The Booking System Project

Below is a breakdown of all four phases of the Booking System project, including what worked, what didn’t, what took the most time, and what I learned.
## Phase 1 – Basic Setup
**What I Did**
- Set up the project environment using Docker
- Connected backend, frontend, and PostgreSQL
- Tested login, registration, and basic reservation flow

**What Worked**
- Docker containers ran successfully
- Database tables created correctly
- Basic login and reservation features functioned

**What Didn’t Work**
- Some initial database connection issues
- Minor UI bugs in the reservation form

**What Took the Most Time**
- Understanding the project structure
- Fixing early database connection errors

**What I Learned**
- How to run multi-container applications
- How backend and frontend communicate in a booking system
## Phase 2 – Security Improvements
**What I Did**
- Improved SQL queries
- Added validation for user input
- Strengthened role-based access control

**What Worked**
- SQL injection protections
- Admin vs reserver permissions

**What Didn’t Work**
- Some validation rules initially blocked valid inputs
- Needed to adjust error messages

**What Took the Most Time**
- Debugging SQL queries
- Testing access control for different roles

**What I Learned**
- Importance of secure coding practices
- How to validate and sanitize user input
## Phase 3 – Admin & Reservation Logic
**What I Did**
- Implemented resource creation
- Implemented reservation creation
- Fixed reservation conflicts
- Debugged database constraint issues

**What Worked**
- Admin resource management
- Reservation conflict detection

**What Didn’t Work**
- Some reservations failed due to overlapping time logic
- Needed to adjust database constraints

**What Took the Most Time**
- Debugging reservation logic
- Testing edge cases

**What I Learned**
- How to design conflict-free booking logic
- How to debug database constraint violations
## Phase 4 – GDPR & Documentation
**What I Did**
- Wrote Privacy Policy, Terms of Service, Cookie Policy
- Completed GDPR Checklist
- Added improvement plans for ❌ items
- Added database schema screenshots
- Updated `README.md` and repo structure

**What Worked**
- Policies were clear and human-friendly
- GDPR checklist aligned with actual functionality

**What Didn’t Work**
- Reserver accounts cannot edit/delete their data
- No data export or consent withdrawal features

**What Took the Most Time**
- Writing GDPR-compliant policies
- Fixing teacher feedback
- Updating checklist with improvement plans

**What I Learned**
- How GDPR applies to real systems
- How to write clear, user-friendly policies
- How to document compliance properly
## Reflection
Working on this project taught me how security, usability, and compliance all connect in real software development. I learned how to build and debug a full booking system, secure it against common vulnerabilities, and document it according to GDPR requirements. The process helped me understand how backend logic, database design, and user roles interact. Writing the policies and checklist also improved my ability to communicate technical and legal concepts clearly. Overall, this project strengthened both my technical and documentation skills.


## Logbook

See the logbook here: https://github.com/rex-daworker/CyberSecurity/blob/main/logbook.md


## Feedback 

This course was challenging but rewarding. The combination of PortSwigger labs and the Booking System project helped me understand both offensive and defensive security. I especially appreciated the practical approach — building, breaking, fixing, and documenting. The GDPR section also added a real-world perspective on compliance. Overall, the course improved my technical confidence and gave me a clearer understanding of cybersecurity in modern web applications.