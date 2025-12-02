# 🛡️ Booking System Phase 1 — Penetration Test Report (Part 1)

---

## 1️⃣ Introduction

**Tester(s):**  
Name: Rex Odomero Oghenerobo

**Purpose:**  
Perform penetration and functionality testing on the Booking System Phase 1 application to identify critical vulnerabilities in registration, login, and session handling.

**Scope:**  
- **Tested components:**  
  - Registration and login forms  
  - Database schema (`booking_users`, `booking_reservations`, `booking_resources`)  
  - Session cookies and headers  
  - OWASP ZAP scan of endpoints

- **Exclusions:**  
  - Admin panel (not accessible)  
  - External APIs (none present)

**Test approach:**  
Gray-box — database access via Docker, but no backend code modification.

**Test environment & dates:**  
- **Start:** 25 November 2025  
- **End:** 26 November 2025  
- **Environment:**  
  - OS: macOS Monterey  
  - Runtime: Docker Compose  
  - DB: PostgreSQL 13  
  - Browser: Firefox Developer Edition  
  - Proxy: OWASP ZAP 2.16.1

**Assumptions & constraints:**  
- Credentials created manually via registration  
- Limited to local testing (`localhost:8000`)  
- No access to production logs or backend code

---

## 2️⃣ Executive Summary

**Short summary:**  
The Booking System Phase 1 (initial release) contained multiple critical vulnerabilities. Registration worked, but login was exploitable. Passwords were stored in plaintext, SQL injection was possible, and CSRF protection was missing.

**Overall risk level:** 🔴 **High**

**Top 5 immediate actions (reported to dev team):**
1. Fix broken login logic and authentication flow
2. Hash passwords securely using bcrypt or Argon2
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

## 4️⃣ Findings (Part 1)

| ID   | Severity | Finding                        | Description                                           | Evidence / Proof |
|------|----------|--------------------------------|-------------------------------------------------------|------------------|
| F-01 | 🔴 High   | SQL Injection in login form    | Input field allows `' OR '1'='1` injection            | ZAP alert + screenshot |
| F-02 | 🔴 High   | Broken login functionality     | Login bypass possible with crafted input              | Screenshot of login page |
| F-03 | 🔴 High   | Plaintext password storage     | Passwords stored without hashing                      | `SELECT * FROM booking_users` result |
| F-04 | 🟠 Medium | Missing CSRF protection        | No CSRF tokens in forms                               | ZAP alert |
| F-05 | 🟠 Medium | Missing HttpOnly flag          | Session cookie lacks HttpOnly attribute               | ZAP alert headers |

---

## 5️⃣ OWASP ZAP Test Report (Attachment)

**Purpose:**  
To identify vulnerabilities in the Booking System Phase 1 using automated scanning tools.

**Scan details:**
- Manual Explore + Spider + Active Scan
- Target: `http://localhost:8000`
- ZAP version: 2.16.1
- Risk levels: High, Medium, Low
- Alerts: SQL injection, missing headers, broken authentication

**Screenshots:**
- ZAP alerts for SQLi and CSRF  
  ![ZAP Scan](https://github.com/user-attachments/assets/example-scan.png)

**Report file:**  
[📄 zap_report_round1.md](https://github.com/your-repo-path/zap_report_round1.md)

---


