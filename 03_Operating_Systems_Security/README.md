# Operating Systems Security & Hardening (CENFOTEC)

This repository documents security engineering practices focused on OS hardening, administrative auditing, and vulnerability mitigation across Windows and Linux environments.

---

## 1. Windows System Security
### Overview
Focuses on Windows Fundamentals, emphasizing administrative tool utilization to restrict access and harden system integrity.

### Technical Analysis & Logic
* **Administrative Toolset:** Mastered `lusrmgr.msc` for access control and `services.msc` for service lifecycle management.
* **Security Auditing:** Leveraged `Event Viewer` and `Resource Monitor` to baseline system behavior and detect anomalies.
* **Registry & Configuration:** Validated security via `regedit.exe` and configured User Account Control (UAC) as a primary security barrier.

### Engineering Takeaways
1. **Defense-in-Depth:** OS hardening starts at the core; managing local services and registry keys significantly reduces the attack surface.
2. **Administrative Visibility:** Auditing system logs is non-negotiable for detecting unauthorized execution patterns.

* **Deliverable:** [Windows Security Report](./Grupo%201%20-%20TryHackMe%20Windows%20Fundamentals%202%20-%20Seguridad%20en%20Sitemas%20Operativos.pdf)

---

## 2. Linux Security & File System Permissions
### Overview
Fundamental study of the Linux security model, focusing on user/group management and the Linux filesystem permission architecture (LPI Standard).

### Technical Analysis & Logic
* **User/Group Management:** Implementation of secure identity management and privilege separation.
* **Permission Architecture:** Detailed analysis of `chmod`, `chown`, and `chgrp` to enforce Principle of Least Privilege.
* **Special Bits:** Understanding the security implications of SUID, SGID, and Sticky Bits in protecting executable binaries and shared directories.
* **Security Auditing:** Verification of access rights using `ls -l` to ensure data integrity and confidentiality.

### Engineering Takeaways
1. **Principle of Least Privilege:** Correct permission assignment is the foundation of Linux security; over-privileged accounts are the primary vector for system compromise.
2. **Proactive Management:** Documenting configurations and policies is essential for professional system administration and audit compliance.

* **Deliverable:** [Linux Security & Permissions Study](./Trabajo%20cotidiano%20Seguridad%20y%20sistema%20de%20permisos%20de%20archivos%20-%20LPI.pdf)
