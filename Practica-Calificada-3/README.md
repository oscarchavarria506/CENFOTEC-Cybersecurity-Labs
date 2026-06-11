# Web Application Security Exploration & Vulnerability Analysis Lab (DVWA)

## Project Overview
This repository documents hands-on security engineering exercises conducted within a controlled, isolated environment using the Damn Vulnerable Web Application (DVWA) framework. The core objective of this project is to simulate, analyze, and mitigate critical web-based threat vectors aligned with the OWASP Top 10 framework, evaluating execution patterns, asset impacts, and defensive remediation strategies.

## Technologies & Tools Used
* **Vulnerable Testing Environment:** Damn Vulnerable Web Application (DVWA)
* **Vulnerability Framework Focus:** OWASP Top 10 Web Application Security Risks
* **Analysis Methodology:** Black-box / Gray-box security simulation

---

## Technical Vulnerability Analysis & Simulation

### 1. SQL Injection (SQLi)
* **Exploitation Vector:** Input validation bypass within database query fields. Leveraged parameter manipulation (`%`, `' OR '1'='1`) to alter backend SQL statements.
* **Impact & Logic:** Successfully bypassed intended input limits, executing unauthorized queries that forced the database engine to extract and disclose hidden record sets, compromising data confidentiality.

### 2. Directory Traversal / File Inclusion
* **Exploitation Vector:** Exploitation of insufficient path sanitation in parameters handling external file rendering.
* **Impact & Logic:** Manipulated input vectors to traverse restricted file-system directory layers, gaining unauthorized read access to internal local system structures outside the web root directory.

### 3. Cross-Site Request Forgery (CSRF)
* **Exploitation Vector:** Session hijacking via unauthorized state-changing request transmission.
* **Impact & Logic:** Exploited web application reliance on implicit browser authentication states (session cookies) to execute unauthorized administrative state modifications without user validation.

### 4. Stored Cross-Site Scripting (XSS Stored)
* **Exploitation Vector:** Injection of unparsed, persistent JavaScript payloads directly into application parameters designed for data storage (e.g., guestbooks or comment fields).
* **Impact & Logic:** The hostile payload executes inside the browser sessions of any subsequent users viewing the affected resource, allowing session hijacking, token theft, and DOM manipulation.

### 5. Advanced Vector: Blind SQL Injection
* **Exploitation Vector:** Inference-based database structure enumeration using conditional logical queries.
* **Impact & Logic:** Extracted structural properties from the database schema by executing boolean operations or time-based delays, reconstructing metadata without needing direct error messages or data output on the user interface.

### 6. Advanced Vector: Command Injection
* **Exploitation Vector:** Execution of arbitrary operating system commands via input fields directly concatenated into host system shell interfaces.
* **Impact & Logic:** Successfully broke out of the web application layer to interact directly with the underlying operating system environment, validating absolute asset compromise potential.

---

## Core Engineering Takeaways & Remediation Log
1. **Input Sanitation & Parametrization:** Explicitly relying on input filtering is insufficient. Secure web architecture mandates parameterized queries (Prepared Statements) to entirely neutralize SQL Injection vectors.
2. **Output Encoding:** Mitigating persistent XSS vectors requires strict context-aware output encoding to ensure user-supplied data is treated strictly as text, never as executable script blocks within the DOM.
3. **Defense-in-Depth for State Modifications:** CSRF defenses must incorporate cryptographic, non-predictable anti-CSRF tokens tied directly to active user sessions to validate explicit action intent.
