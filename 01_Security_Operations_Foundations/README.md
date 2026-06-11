# Security Operations Foundations (CENFOTEC)

This repository documents a series of security engineering exercises conducted in a controlled environment. The objective is to evaluate infrastructure integrity, identify attack vectors, and implement defensive remediation strategies across network and application layers.

---

## 1. Network Traffic Analysis & Port Scanning
### Project Overview
Focuses on reconnaissance and packet-level diagnostics to map network exposure and demonstrate the critical necessity of transport-layer encryption.

### Technical Analysis & Logic
* **Network Mapping:** Conducted subnet-wide enumeration using Zenmap/Nmap. Performed service identification to detect open ports (e.g., Port 80) and active services.
* **Vulnerability Enumeration:** Leveraged `nmap --script vuln` to probe infrastructure, identifying exposure to risks like XSS and CSRF.
* **Packet Inspection (Wireshark):**
    * **HTTP Vulnerability:** Intercepted POST request parameters in plaintext, demonstrating high-risk credential harvesting due to lack of encryption.
    * **HTTPS Mitigation:** Validated TLS protocol implementation, observing the transition from plaintext to opaque "Application Data," effectively neutralizing Man-in-the-Middle (MitM) sniffing.

### Engineering Takeaways
1. **Attack Surface Management:** Constant reconnaissance is required to identify shadow services before malicious actors do.
2. **Data-in-Transit Security:** Plaintext protocols are obsolete for sensitive data; TLS is the mandatory standard for integrity and confidentiality.

* **Deliverable:** [Download Report](./Entregable%201%20Análisis%20de%20Tráfico%20y%20Escaneo%20de%20Puertos.pdf)

---

## 2. Network Security Practice (Azure NSG)
### Project Overview
Infrastructure hardening exercise focused on cloud-native security via Microsoft Azure.

### Technical Analysis & Logic
* **NSG Configuration:** Designed granular Inbound/Outbound security rules to segment traffic and restrict access to critical VM assets.
* **Threat Simulation & Mitigation:** Configured firewall policies to mitigate specific vectors: RDP Brute Force, DDoS, and lateral movement.
* **Traffic Validation:** Utilized Azure Network Watcher to audit `Access Denied` logs, confirming the effectiveness of traffic flow control and egress filtering.

### Engineering Takeaways
1. **Defense-in-Depth:** Network Security Groups (NSGs) act as the primary micro-segmentation layer in cloud architectures.
2. **Continuous Monitoring:** Firewall logs (Network Watcher) are essential to validate rule efficiency and detect abnormal egress patterns.

* **Deliverable:** [Download Report](./Práctica%20Calificada%202.pdf)

---

## 3. Web Application Attacks (DVWA)
### Project Overview
OWASP Top 10 simulation using DVWA to evaluate exploitation patterns and implement code-level remediation.

### Technical Analysis & Logic
* **SQL Injection (SQLi):** Exploited input validation bypasses via parameter manipulation to force unauthorized database schema disclosure.
* **XSS & CSRF:** Simulated session hijacking via persistent JavaScript injection (Stored XSS) and forced state-changing requests (CSRF).
* **Directory Traversal:** Manipulated path parameters to traverse system directories outside the web root.

### Engineering Takeaways
1. **Parameterized Queries:** SQLi is fully mitigated by using prepared statements, not just input filtering.
2. **Context-Aware Encoding:** XSS defense requires strict encoding of user-supplied data at the DOM level.
3. **Session Integrity:** CSRF tokens are critical to validate the intent of state-changing actions.

* **Deliverable:** [Download Report](./Practica%20Calificada%203%20-%20Ataques%20en%20Aplicaciones%20Web.pdf)
