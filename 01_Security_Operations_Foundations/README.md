# Security Operations Foundations (CENFOTEC)

This repository documents high-level engineering exercises focused on infrastructure protection, network diagnostics, and vulnerability exploitation methodologies. The lab environment simulates real-world attack vectors to evaluate system integrity, traffic flow control, and defensive hardening strategies.

## Technologies & Tools Used
* **Network Analysis:** Wireshark, Zenmap (Nmap)
* **Cloud Security:** Microsoft Azure Network Watcher, NSGs
* **Web Security:** DVWA (Damn Vulnerable Web Application)
* **Methodology:** Reconnaissance, Traffic Inspection, Threat Mitigation

---

## Technical Analysis & Lab Deliverables

### 1. Network Traffic Analysis & Port Scanning
* **Objective:** Perform network reconnaissance and validate data transmission security.
* **Analysis & Logic:** * **Scanning:** Conducted subnet-wide enumeration using Zenmap/Nmap to map active hosts and identify exposed services.
    * **Packet Analysis:** Utilized Wireshark to perform a comparative analysis between HTTP and HTTPS. Demonstrated how clear-text HTTP facilitates credential harvesting, whereas TLS/HTTPS ensures payload encryption and confidentiality, effectively neutralizing packet sniffing threats.
* **Deliverable:** [Download PDF](./Entregable%201%20Análisis%20de%20Tráfico%20y%20Escaneo%20de%20Puertos.pdf)

### 2. Network Security Practice (Azure NSG)
* **Objective:** Implementation of defensive cloud network architecture.
* **Analysis & Logic:** * **NSG Hardening:** Configured Azure Network Security Groups (NSGs) with granular inbound/outbound rules to block unauthorized traffic.
    * **Threat Mitigation:** Simulated and blocked attack vectors including Brute Force (RDP), DDoS, and lateral movement attempts. Used Azure Network Watcher to verify "Access Denied" logs, validating effective traffic flow control.
* **Deliverable:** [Download PDF](./Práctica%20Calificada%202.pdf)

### 3. Web Application Attacks (DVWA)
* **Objective:** OWASP Top 10 exploitation and remediation simulation.
* **Analysis & Logic:** * **Attack Vectors:** Executed SQL Injection, Stored XSS, CSRF, and Directory Traversal. Manipulated input parameters to bypass database validation and hijack browser sessions.
    * **Remediation Logic:** Evaluated the implementation of input parametrization, secure output encoding, and session tokenization to neutralize web-based compromise risks.
* **Deliverable:** [Download PDF](./Practica%20Calificada%203%20-%20Ataques%20en%20Aplicaciones%20Web.pdf)

---

## Engineering Takeaways
1. **Network Hygiene:** Proper port configuration and network segmentation are the first line of defense against lateral movement.
2. **Data Confidentiality:** Transport Layer Security (TLS) is non-negotiable for any infrastructure involving credential or sensitive data transmission.
3. **Proactive Hardening:** Defending web applications requires moving beyond basic filtering toward architectural solutions like prepared statements and context-aware security headers.
