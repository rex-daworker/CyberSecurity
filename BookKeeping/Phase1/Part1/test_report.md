# 🛡️ Booking System Phase 1 — Penetration Test Report

---

## 1️⃣ Introduction

**Tester(s):**  
Name: Rex Odomero Oghenerobo

**Purpose:**  
Identify vulnerabilities in registration and authentication flows of the Booking System Phase 1 web application.
 
**Scope:**  
- **Tested components:**  
  - Registration and login forms  
  - Database schema (`booking_users`, `booking_reservations`, `booking_resources`)  
  - Frontend session handling  
  - OWASP ZAP scan of all endpoints

- **Exclusions:**  
  - Admin panel (not accessible)  
  - External APIs (none present)

- **Test approach:**  
  Gray-box — database access and source code visibility via Docker, but no backend code modification.

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

**Setup screenshots:**
1. Docker Compose setup  
   ![Docker Compose](https://github.com/user-attachments/assets/17cfcd82-7f05-445d-ad73-486ce5452374)

2. Web app running in browser  
   ![Browser View](https://github.com/user-attachments/assets/acd87277-3b0f-4dfb-93af-8f909ae94ac2)

3. PostgreSQL user data inspection  
   ![Database Query](https://github.com/user-attachments/assets/7d49e694-7322-4bbe-ad60-af9794840042)

---

## 2️⃣ Executive Summary

**Short summary:**  
The Booking System Phase 1 contains critical vulnerabilities in authentication and session handling. Registration works, but login fails consistently. Passwords are hashed correctly using bcrypt, but the login logic appears broken.

**Overall risk level:** 🔴 **High**

**Top 5 immediate actions:**
1. Fix broken login logic and authentication flow
2. Ensure bcrypt password verification works correctly
3. Sanitize inputs to prevent SQL injection
4. Implement CSRF protection for all forms
5. Set HttpOnly and Secure flags on session cookies

---

## 3️⃣ Severity Scale & Definitions

| Severity Level | Description | Recommended Action |
|----------------|-------------|--------------------|
| 🔴 High | A serious vulnerability that can lead to full system compromise or data breach (e.g., SQL Injection, Remote Code Execution). | Immediate fix required |
| 🟠 Medium | A significant issue that may require specific conditions or user interaction (e.g., XSS, CSRF). | Fix ASAP |
| 🟡 Low | A minor issue or configuration weakness (e.g., server version disclosure). | Fix soon |
| 🔵 Info | No direct risk, but useful for system hardening (e.g., missing security headers). | Monitor and fix in maintenance |

---

## 4️⃣ Findings

| ID   | Severity | Finding                        | Description                                           | Evidence / Proof |
|------|----------|--------------------------------|-------------------------------------------------------|------------------|
| F-01 | 🔴 High   | SQL Injection in registration  | Input field allows `' OR '1'='1` injection            | ZAP alert + screenshot |
| F-02 | 🔴 High   | Broken login functionality     | Login fails despite correct credentials and hashed password | Screenshot of login page + DB query |
| F-03 | 🟠 Medium | Password hash verification broken | Passwords are hashed with bcrypt, but login logic fails | `SELECT * FROM booking_users` result |
| F-04 | 🟠 Medium | Missing CSRF protection        | No CSRF tokens in forms                               | ZAP alert |
| F-05 | 🟠 Medium | Missing HttpOnly flag          | Session cookie lacks HttpOnly attribute               | ZAP alert headers |

---

## 5️⃣ OWASP ZAP Test Report

**Scan purpose:**  
To identify vulnerabilities in the Booking System Phase 1 using OWASP ZAP automated scanning tools.

**Scan details:**
- Manual Explore + Spider + Active Scan
- Target: `http://localhost:8001`
- ZAP version: 2.16.1
- Risk levels: High, Medium, Low
- Key alerts:
  - SQL Injection (registration form)
  - Absence of Anti-CSRF Tokens
  - Missing HttpOnly flag on cookies

**Screenshots:**
- ZAP alert for CSRF  
  ![ZAP CSRF Alert](https://github.com/user-attachments/assets/261a4625-e8f9-4f24-8752-9ba42ffa5fbf)

**Report file:**  
[📄 zap_report_round2.md](https://github.com/your-repo-path/zap_report_round2.md)

---


