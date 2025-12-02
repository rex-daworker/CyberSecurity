# ZAP by Checkmarx Scanning Report

Generated with ZAP on Tue 2 Dec 2025, at 17:28:11  
ZAP Version: 2.16.1  
ZAP by Checkmarx

---

## Contents

- About this report
  - Report parameters
- Summaries
  - Alert counts by risk and confidence
  - Alert counts by site and risk
  - Alert counts by alert type
- Alerts
  - Risk = Medium, Confidence = Low (1)
  - Risk = Informational, Confidence = Medium (1)
- Appendix
  - Alert types

---

## About this report

### Report parameters

#### Contexts
No contexts were selected, so all contexts were included by default.

#### Sites
The following sites were included:
- `http://localhost:8001`

(If no sites were selected, all sites were included by default.)  
An included site must also be within one of the included contexts for its data to be included in the report.

#### Risk levels
Included: High, Medium, Low, Informational  
Excluded: None

#### Confidence levels
Included: User Confirmed, High, Medium, Low  
Excluded: User Confirmed, High, Medium, Low, False Positive

---

## Summaries

### Alert counts by risk and confidence

This table shows the number of alerts for each level of risk and confidence included in the report. (Percentages in brackets represent the count as a percentage of total alerts.)

| Risk / Confidence | User Confirmed | High | Medium | Low | Total |
|---:|:---:|:---:|:---:|:---:|:---:|
| High | 0 (0.0%) | 0 (0.0%) | 0 (0.0%) | 0 (0.0%) | 0 (0.0%) |
| Medium | 0 (0.0%) | 0 (0.0%) | 0 (0.0%) | 1 (50.0%) | 1 (50.0%) |
| Low | 0 (0.0%) | 0 (0.0%) | 0 (0.0%) | 0 (0.0%) | 0 (0.0%) |
| Informational | 0 (0.0%) | 0 (0.0%) | 1 (50.0%) | 0 (0.0%) | 1 (50.0%) |
| **Total** | 0 (0.0%) | 0 (0.0%) | 1 (50.0%) | 1 (50.0%) | 2 (100%) |

---

### Alert counts by site and risk

This table shows, for each site for which one or more alerts were raised, the number of alerts raised at each risk level. (Alerts with confidence "False Positive" have been excluded from these counts. The numbers in brackets are the number of alerts raised for the site at or above that risk level.)

| Site | High (= High) | Medium (>= Medium) | Low (>= Low) | Informational (>= Informational) |
|---|:---:|:---:|:---:|:---:|
| http://localhost:8001 | 0 (0) | 1 (1) | 0 (1) | 1 (2) |

---

### Alert counts by alert type

This table shows the number of alerts of each alert type, together with the alert type's risk level.

| Alert type | Risk | Count |
|---|---|---:|
| Absence of Anti-CSRF Tokens | Medium | 1 (50.0%) |
| User Agent Fuzzer | Informational | 12 (600.0%) |
| **Total** |  | 2 |

> Note: The "User Agent Fuzzer" count displays 12 (600.0%) in the original report; I preserved these original numbers.

---

## Alerts

### Risk = Medium, Confidence = Low (1)

- Site: http://localhost:8001 (1)

#### Absence of Anti-CSRF Tokens (1)

- Request: `GET http://localhost:8001/register`

Alert tags:
- [OWASP_2021_A01](https://owasp.org/Top10/A01_2021-Broken_Access_Control/)
- POLICY_QA_STD
- POLICY_PENTEST
- [SYSTEMIC](https://www.zaproxy.org/docs/desktop/addons/common-library/alerttags/#systemic)
- WSTG-v42-SESS-05
- OWASP_2017_A05
- [CWE-352](https://cwe.mitre.org/data/definitions/352.html)
- POLICY_DEV_STD

Alert description:

No Anti-CSRF tokens were found in a HTML submission form.

A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.

CSRF attacks are effective in a number of situations, including:
- The victim has an active session on the target site.
- The victim is authenticated via HTTP auth on the target site.
- The victim is on the same local network as the target site.

CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.

Other info:
No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF, _token, _csrf_token, _csrfToken] was found in the following HTML form: [Form 1: "birthdate" "password" "username" ].

Request (headers):

```
GET http://localhost:8001/register HTTP/1.1
host: localhost:8001
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:145.0) Gecko/20100101 Firefox/145.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: en-US,en;q=0.5
Connection: keep-alive
Referer: http://localhost:8001/
Upgrade-Insecure-Requests: 1
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Sec-Fetch-User: ?1
Priority: u=0, i
```

Request body (0 bytes): empty

Response (status and headers):

```
HTTP/1.1 200 OK
content-type: text/html
content-security-policy: default-src 'self'; script-src 'self'; style-src 'self'; img-src 'self'; frame-ancestors 'none'; form-action 'self';
x-frame-options: DENY
x-content-type-options: nosniff
vary: Accept-Encoding
content-length: 3026
date: Tue, 02 Dec 2025 15:02:38 GMT
```

Response body (3026 bytes):

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>User Registration</title>
    <link href="/static/tailwind.css" rel="stylesheet"> <!-- Link to Tailwind CSS -->
</head>

<body class="flex flex-col min-h-screen bg-gray-100 text-gray-900">
  <main class="flex-grow">
    <div class="container mx-auto p-4">
        <div class="bg-white shadow-md rounded-lg p-6 mt-6 max-w-lg mx-auto">
            <h1 class="text-2xl font-bold mb-4 text-center">Register</h1>
            <form action="/register" method="POST">
                <div class="mb-4">
                    <label for="username" class="block text-sm font-medium text-gray-700 font-bold">Email</label>
                    <input type="email" id="username" name="username" placeholder="Enter your email" required class="mt-1 block w-full px-3 py-2 border rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm">
                </div>
                <div class="mb-4">
                    <label for="password" class="block text-sm font-medium text-gray-700 font-bold">Password</label>
                    <input type="password" id="password" name="password" placeholder="Create a password" required class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm">
                </div>
                <div class="mb-4">
                    <label for="birthdate" class="block text-sm font-medium text-gray-700 font-bold">Birthdate</label>
                    <input type="date" id="birthdate" name="birthdate" required class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm">
                </div>
                <div class="mb-4">
                    <label for="role" class="block text-sm font-medium text-gray-700 font-bold">Role</label>
                    <select id="role" name="role" required class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm">
                        <option value="reserver">Reserver</option>
                        <option value="administrator">Administrator</option>
                    </select>
                </div>
                <div class="flex justify-between space-x-4">
                    <button type="submit" class="inline-block bg-blue-500 text-white py-2 px-4 rounded hover:bg-blue-600 w-1/2">Register</button>
                    <a href="/" class="inline-block bg-gray-500 text-white py-2 px-4 rounded hover:bg-gray-600 w-1/2 text-center">Cancel</a>
                </div>
            </form>
        </div>
    </div>
  </main>
  <div id="footer-placeholder"></div>
  <script src="/static/footer.js"></script>
</body>

</html>
```

Evidence:
```
<form action="/register" method="POST">
```

Solution (summary):
- Phase: Architecture and Design — Use a vetted library or framework that supports anti-CSRF, e.g., OWASP CSRFGuard.
- Phase: Implementation — Ensure application is free of XSS, generate unique, unpredictable nonces for each form and verify them on receipt, and avoid GET for state-changing requests.
- Consider additional protections like separate confirmation requests for dangerous operations, use ESAPI Session Management control, and optionally check the HTTP Referer header (with caution due to proxies/privacy).

---

### Risk = Informational, Confidence = Medium (1)

- Site: http://localhost:8001 (1)

#### User Agent Fuzzer (1)

- Request: `POST http://localhost:8001/register`

Alert tags:
- CUSTOM_PAYLOADS
- POLICY_PENTEST
- SYSTEMIC

Alert description:
Check for differences in response based on fuzzed User Agent (e.g., mobile sites, access as a Search Engine Crawler). Compares the response status code and the hash code of the response body with the original response.

Request (headers):

```
POST http://localhost:8001/register HTTP/1.1
host: localhost:8001
user-agent: Mozilla/4.0 (compatible; MSIE 8.0; Windows NT 6.1)
pragma: no-cache
cache-control: no-cache
content-type: application/x-www-form-urlencoded
referer: http://localhost:8001/register
content-length: 83
```

Request body (83 bytes):

```
username=foo-bar%40example.com&password=ZAP&birthdate=2025-12-02&role=administrator
```

Response (status and headers):

```
HTTP/1.1 200 OK
content-type: text/html
content-security-policy: default-src 'self'; script-src 'self'; style-src 'self'; img-src 'self'; frame-ancestors 'none'; form-action 'self';
x-frame-options: DENY
x-content-type-options: nosniff
vary: Accept-Encoding
content-length: 1322
date: Tue, 02 Dec 2025 15:10:53 GMT
```

Response body (1322 bytes):

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Staus</title>
    <link href="/static/tailwind.css" rel="stylesheet">
</head>

<body class="flex flex-col min-h-screen bg-gray-100 text-gray-900">
    <main class="flex-grow">
        <div class="container mx-auto p-4">
            <div class="bg-white shadow-md rounded-lg p-6 mt-6 max-w-lg mx-auto">
                <h1 class="text-2xl font-bold mb-4 text-center">Status</h1>

                <!-- Status message box -->
                <div id="status-box" class="hidden p-4 rounded-md mb-4">
                    <div id="status-title" class="font-bold mb-1"></div>
                    <p id="status-message"></p>
                </div>

                <div class="flex justify-between space-x-4">
                    <a href="/"
                        class="block w-full bg-blue-500 text-white py-2 px-4 rounded text-center hover:bg-blue-600">
                        Back to home
                    </a>
                </div>
            </div>
        </div>
    </main>

    <div id="footer-placeholder"></div>
    <script src="/static/footer.js"></script>
    <script src="/static/status.js"></script>
</body>

</html>
```

Parameter:
```
Header User-Agent
```

Attack:
```
Mozilla/4.0 (compatible; MSIE 8.0; Windows NT 6.1)
```

---

## Appendix

### Alert types

1. Absence of Anti-CSRF Tokens

   - Source: raised by a passive scanner ([Absence of Anti-CSRF Tokens](https://www.zaproxy.org/docs/alerts/10202/))
   - CWE ID: [352](https://cwe.mitre.org/data/definitions/352.html)
   - WASC ID: 9
   - References:
     1. https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html
     2. https://cwe.mitre.org/data/definitions/352.html

2. User Agent Fuzzer

   - Source: raised by an active scanner ([User
