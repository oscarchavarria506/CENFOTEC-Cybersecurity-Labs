# Operating Systems Security & Hardening (CENFOTEC)

This repository documents security engineering practices focused on Windows system hardening, administrative tool utilization, and vulnerability mitigation. The labs center on the "Windows Fundamentals" framework, applying security policies to protect critical OS components.

---

## 1. Windows System Hardening & Configuration
### Overview
Hands-on application of OS-level security configurations using administrative tools to restrict access, monitor processes, and harden system integrity.

### Technical Analysis & Logic
* **Administrative Toolset:** Mastered the use of `lusrmgr.msc` (Local Users and Groups) and `services.msc` for granular access control and service management.
* **System Monitoring:** Leveraged `Event Viewer` and `Resource Monitor` to perform security audits, identifying unauthorized execution patterns and system resource anomalies.
* **Registry & Configuration:** Explored the Windows Registry (`regedit.exe`) and `System Configuration` (`msconfig`) to validate system-wide security settings and startup integrity.
* **Privilege Management:** Evaluated User Account Control (UAC) settings as a primary barrier against unauthorized administrative changes.

### Engineering Takeaways
1. **Granular Permission Control:** Security isn't just about passwords; it requires deep understanding of NTFS and Advanced Security Properties to restrict execution and writing privileges on critical directories.
2. **Administrative Visibility:** Tools like Event Viewer and Resource Monitor are essential for any security engineer to baseline system behavior and detect deviations.
3. **Defense-in-Depth:** Hardening starts at the OS core. Managing local services and registry keys directly significantly reduces the attack surface of a Windows endpoint.

---

## 2. Lab Deliverables
* **[Windows Security Fundamentals - Lab Report](./Grupo%201%20-%20TryHackMe%20Windows%20Fundamentals%202%20-%20Seguridad%20en%20Sitemas%20Operativos.pdf)**
