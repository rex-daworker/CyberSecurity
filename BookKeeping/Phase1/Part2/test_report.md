# 🛡️ Booking System Phase 1 — Penetration Test Report (Part 2)

---

## 1️⃣ Introduction

**Tester(s):**  
Name: Rex Odomero Oghenerobo

**Purpose:**  
Re-test the Booking System application after developers released Phase 1 Part 2 fixes. The goal was to verify whether the vulnerabilities reported in Part 1 were addressed.

**Scope:**  
- **Tested components:**  
  - Registration and login forms  
  - Database schema (`booking_users`)  
  - Frontend session handling  
  - OWASP ZAP scan of all endpoints

- **Exclusions:**  
  - Admin panel (not accessible)  
  - External APIs (none present)

**Test approach:**  
Gray-box — database access via Docker, but no backend code modification.

**Test environment & dates:**  
- **Start:** 01 December 2025  
- **End:** 02 December 2025  
- **Environment:**  
  - OS: macOS Monterey  
  - Runtime: Docker Compose  
  - DB: PostgreSQL 13  
  - Browser: Firefox Developer Edition  
  - Proxy: OWASP ZAP 2.16.1

**Assumptions & constraints:**  
- Credentials created manually via registration  
- Limited to local testing (`localhost:8001`)  
- No access to production logs or backend code

**Setup screenshots (Part 2):**

1. Docker Compose containers running (`cybersec-db-phase1-part2`, `cybersec-web-phase1-part2`)  
   <img width="1280" height="800" alt="Screenshot 2025-12-02 at 18 05 49-1" src="https://github.com/user-attachments/assets/d4ee2d08-3781-4a36-abba-4db0643f9ed4" />


2. Web app running in browser at `http://localhost:8001`  
   <img width="1276" height="800" alt="Screenshot 2025-12-02 at 14 37 42" src="https://github.com/user-attachments/assets/b89249b7-0f8e-4ef1-ba92-f52648de83b2" />


3. PostgreSQL query showing user data with bcrypt-hashed password  
   <img width="620" height="364" alt="Screenshot 2025-12-02 at 17 47 08" src="https://github.com/user-attachments/assets/a4eeb3d5-00b1-4879-aead-af0d88453743" />


4. Web logs showing DB connection success  
   <img width="1280" height="800" alt="Screenshot 2025-12-02 at 18 10 55-1" src="https://github.com/user-attachments/assets/3c5412c0-27d0-44b0-90ca-cb8a9bdc2eca" />


---

## 2️⃣ Executive Summary

**Short summary:**  
Phase 1 Part 2 fixed some vulnerabilities (passwords now hashed, DB connection stable), but login remains broken. ZAP scans show SQL injection mitigated, but CSRF protection is still missing and cookies lack security flags.

**Overall risk level:** 🟠 **Medium–High**

**Top 5 immediate actions (Part 2):**
1. Fix broken login logic and bcrypt verification  
2. Add CSRF tokens to all forms  
3. Set HttpOnly and Secure flags on cookies  
4. Continue sanitizing inputs to prevent SQL injection (appears fixed)  
5. Improve error handling and logging for authentication failures  

---

## 3️⃣ Severity Scale & Definitions

| Severity Level | Description | Recommended Action |
|----------------|-------------|--------------------|
| 🔴 High | A serious vulnerability that can lead to full system compromise or data breach. | Immediate fix required |
| 🟠 Medium | A significant issue requiring user interaction or specific conditions. | Fix ASAP |
| 🟡 Low | A minor issue or configuration weakness. | Fix soon |
| 🔵 Info | No direct risk, but useful for hardening. | Monitor and fix in maintenance |

---

## 4️⃣ Findings (Part 2)

| ID   | Severity | Finding                        | Description                                           | Evidence / Proof |
|------|----------|--------------------------------|-------------------------------------------------------|------------------|
| F-01 | 🟠 Medium | SQL Injection mitigated        | Injection attempts no longer bypass login             | ZAP scan result |
| F-02 | 🔴 High   | Broken login functionality     | Login fails despite correct credentials and hashed password | Screenshot of login attempt + DB query |
| F-03 | 🟠 Medium | Password hash verification broken | Passwords hashed with bcrypt, but login logic fails   | Screenshot of DB query |
| F-04 | 🟠 Medium | Missing CSRF protection        | No CSRF tokens in forms                               | ZAP alert screenshot |
| F-05 | 🟠 Medium | Missing HttpOnly flag          | Session cookie lacks HttpOnly attribute               | ZAP alert headers |

---

## 5️⃣ OWASP ZAP Test Report

**Purpose:**  
To verify whether vulnerabilities identified in Part 1 were fixed in Part 2.

**Scan details:**
- Manual Explore + Spider + Active Scan
- Target: `http://localhost:8001`
- ZAP version: 2.16.1
- Risk levels: High, Medium, Low
- Key alerts:
  - SQL Injection mitigated  
  - Absence of Anti-CSRF Tokens  
  - Missing HttpOnly flag on cookies  

**Screenshots (Part 2):**

- ZAP alert for CSRF  
<img width="1280" height="800" alt="Screenshot 2025-12-02 at 17 19 56" src="https://github.com/user-attachments/assets/8bf0c9b0-a631-4f03-ab0e-eb9c30155b71" />


- ZAP cookie alert  
  <img width="1280" height="800" alt="Screenshot 2025-12-02 at 17 23 12" src="https://github.com/user-attachments/assets/670da01e-7696-4b6a-91b2-da824dda1163" />


**Report file:**  
[📄 zap_report_round2.md](https://github.com/rex-daworker/CyberSecurity/blob/main/BookKeeping/Phase1/Part2/zap_report_round2.md)


---
