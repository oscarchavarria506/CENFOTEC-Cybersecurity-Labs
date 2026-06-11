# Security Operations & Incident Response (CENFOTEC)

This repository documents the operational security lifecycle, including vulnerability analysis, system hardening, and forensic incident investigation. The focus is on maintaining the CIA triad (Confidentiality, Integrity, Availability) through proactive monitoring and rigorous administrative policies.

---

## 1. Operational Security Assessment & Strategy
### Overview
Analysis of organizational security deficiencies and the implementation of operational controls to ensure business continuity.

### Technical Analysis
* **Gap Analysis:** Evaluated critical failures in operational security, including shared credential usage, delayed patching cycles, and lack of audit logging.
* **Resilience Framework:** Developed mitigation strategies based on physical security, data backup integrity, and granular access control policies.
* **Risk Management:** Applied principles of security operations to align IT infrastructure with enterprise continuity requirements.
* **Deliverable:** [Operational Security Analysis Report](./Practica%201.pdf)

---

## 2. Digital Forensics & Incident Investigation
### Overview
Investigation of a compromised Windows environment to reconstruct the attack timeline and identify persistence mechanisms.

### Technical Analysis
* **Forensic Reconstruction:** Analyzed Event Logs (Event IDs 4688, 4104, 4656) to correlate malicious process execution and identify lateral movement.
* **Persistence Identification:** Manual detection of malicious scheduled tasks, registry modifications (Run keys), and rogue services used by attackers for long-term access.
* **C2 Communication:** Identification of external Command & Control (C2) server communication patterns and DNS poisoning attempts.
* **Deliverable:** [Windows Incident Investigation Report](./Tarea%201.pdf)

---

## 3. Account Management & Identity Governance
### Overview
Comparative analysis of identity and access management (IAM) tools across Windows, Linux, and macOS environments, with a deep dive into Active Directory.

### Technical Analysis
* **Identity Lifecycle:** Practical management of User Accounts, Organizational Units (OUs), and Group Policy Objects (GPOs) within Active Directory.
* **Administrative Hardening:** Implementation of Delegated Control and secure password policies (PowerShell-based automation).
* **Cross-Platform Audit:** Evaluating management tools (e.g., AD, local policies, terminal-based user management) to determine the most effective environment for large-scale enterprise auditing.
* **Deliverable:** [IAM & Active Directory Lab](./Practica%20%233%20-%20Seguridad%20de%20Operaciones.pdf)

---

## Engineering Takeaways
1. **Audit Logs are the Source of Truth:** Incident response is impossible without centralized, reliable logging (Event Viewer/SIEM). Correlating timestamps is the most effective way to reconstruct an attacker's steps.
2. **Persistence is a Multi-Layered Threat:** Attackers don't just rely on one method; they combine scheduled tasks, service configuration, and registry tampering to maintain access.
3. **IAM as a Security Pillar:** Identity is the new perimeter. Implementing strict OUs, GPOs, and delegated administration is essential to prevent internal threats and lateral movement.
