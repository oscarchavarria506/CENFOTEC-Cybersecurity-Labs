# Operating Systems Engineering (CENFOTEC)

This repository documents hands-on engineering labs and a capstone project focused on operating system administration, infrastructure deployment, and automation. All environments were architected, deployed, and tested within **VirtualBox virtualization environments**, simulating real-world enterprise infrastructure.

---

## 1. Environment Infrastructure & Virtualization
### Overview
All labs were executed in an isolated, virtualized environment using **VirtualBox**. This architecture allowed for complex multi-node network simulation, kernel-level testing, and risk-free system administration experiments.

### Technical Scope
* **Platform:** VirtualBox (Virtualization & Snapshot-based testing).
* **OS Distribution:** Linux (Debian-based) and Windows Server 2022.
* **Core Competencies:** CLI administration, user/group management, service configuration, and shell scripting.

---

## 2. Lab Deliverables

### Lab 1: Linux CLI & File System Management
* **Focus:** Kernel interaction via shell, file system hierarchy, and permission structures.
* **Key Skills:** `chmod`/`chown` management, directory tree architecture, and process monitoring (`top`).
* **Deliverable:** [View Lab Report](./Primer%20Practica%20–%20Segunda%20Parte.pdf)

### Lab 2: OS Administration & Automation (PowerShell)
* **Focus:** Windows Server administration and task automation.
* **Key Skills:** PowerShell scripting (Loops, Conditionals), Server Manager roles, and system configuration.
* **Deliverable:** [View Part I](./Segunda%20Practica%20–%20Primera%20Parte.pdf) | [View Part II](./Segunda%20Practica%20-%20Parte%20II.pdf)

### Lab 3: Active Directory & Domain Services
* **Focus:** Enterprise identity management and GPO implementation.
* **Key Skills:** AD DS installation, Domain Controller promotion, DNS configuration, and Group Policy Object (GPO) hardening.
* **Deliverable:** [View Part I](./Tercera%20Practica%20-%20Parte%20I.pdf) | [View Part II](./Tercera%20Practica%20-%20Parte%20II.pdf)

---

## 3. Capstone Project: TechSolutions Corp Infrastructure
### Overview
Design and deployment of a robust IT infrastructure for a growing tech enterprise, incorporating server roles, security policies, and service optimization.

### Engineering Logic
* **Design:** Architectural planning of domain structures and network integration (DHCP, DNS, AD).
* **Implementation:** Deployment of critical server roles, hardened security policies, and performance tuning.
* **Documentation:** Comprehensive project design and implementation report.
* **Deliverable:** [View Final Project Report](./Sistemas%20Operativos%20Proyecto%20Final.pdf)

---

## Engineering Takeaways
1. **Virtualization Efficiency:** VirtualBox snapshots were utilized as a critical engineering tool for version control at the OS level, allowing rapid recovery during configuration errors.
2. **Infrastructure-as-Code (IaC) Mindset:** PowerShell scripting and Bash automation were central to scaling configuration efforts, reducing human error in repetitive tasks.
3. **Defense-in-Depth:** Enterprise OS management is not just about functionality, but about rigorous policy enforcement through GPOs and granular permission sets (NTFS/Linux ownership).
