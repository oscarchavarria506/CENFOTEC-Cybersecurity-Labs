# Network Traffic Analysis & Port Scanning Lab

## Project Overview
This repository contains a hands-on cybersecurity lab focused on network reconnaissance and packet analysis completed at CENFOTEC. The project simulates a real-world security audit, split into two main phases: identifying active hosts and vulnerabilities via network scanning, and analyzing credential transmission over unencrypted (HTTP) versus encrypted (HTTPS) protocols.

## Technologies & Tools Used
* **Network Scanning:** Zenmap (Nmap GUI)
* **Packet Inspection:** Wireshark
* **Environments:** Microsoft Azure (Virtual Machines via Bastion)
* **Protocols Analyzed:** TCP/IP, HTTP, HTTPS, TLS, MSRPC, SMB

---

## Lab Execution & Technical Logic

### Phase 1: Reconnaissance and Port Scanning (Zenmap)
* **Network Mapping:** Conducted a subnet-wide quickscan to map active infrastructure and enumerate live hosts.
* **Service Verification:** Investigated open ports across target IPs, identifying critical exposed services like HTTP (Port 80).
* **Vulnerability Scanning:** Executed targeted Nmap scripts (nmap --script vuln) targeting web infrastructure to detect exposure to common vulnerabilities such as Cross-Site Scripting (XSS) and Cross-Site Request Forgery (CSRF).

### Phase 2: Packet Analysis & Credential Harvesting (Wireshark)
* **Unencrypted Traffic Risk (HTTP):** Captured and analyzed a simulated web login attempt using basic HTTP. By applying specific source/destination IP filters and inspecting POST request parameters (application/x-www-form-urlencoded), credentials were intercepted and read in plaintext due to the complete lack of protocol encryption.
* **Encrypted Traffic Validation (HTTPS):** Captured the exact same authentication workflow over an HTTPS-secured interface. Verified that HTTP data streams are replaced by encrypted payloads (Application Data over TLS), successfully mitigating credential harvesting and packet sniffing threats.

---

## Key Security Takeaways
1. **Visibility is Security:** Consistent port and vulnerability scanning are non-negotiable baselines to evaluate active attack surfaces before malicious actors do.
2. **The Imperative of Transport Layer Security:** Plaintext HTTP exposes enterprise networks to simple Man-in-the-Middle (MitM) attacks. Enforcing HTTPS/TLS is critical to ensure data integrity and confidentiality during transmission.
