# Network Security & Infrastructure Defense (CENFOTEC)

This repository documents the engineering implementation of secure network architectures, access control mechanisms, and defensive frameworks. The projects cover the transition from traditional perimeter defense to a modern "Zero Trust" architecture, incorporating industry-standard controls.

---

## 1. Zero Trust Methodology & Architecture
### Overview
Strategic implementation of "Zero Trust" for a cloud-hybrid enterprise environment, focusing on minimizing attack surfaces and preventing unauthorized lateral movement.

### Technical Analysis
* **Core Philosophy:** Implicit trust is replaced by explicit verification. No entity, internal or external, is granted automatic access.
* **Engineering Strategies:**
    * **Micro-segmentation:** Dividing the network into secure zones to contain potential breaches.
    * **Dynamic Authentication:** Verification of access flows regardless of the origin (remote or internal).
    * **Data Classification:** Tagging sensitive assets to apply granular security policies.
* **Deliverable:** [Case Study Report](./Caso%20de%20Estudio%201.pdf)

---

## 2. Access Control & Traffic Flow Engineering
### Overview
Practical implementation of Extended Access Control Lists (ACLs) to enforce granular traffic filtering at the network layer.

### Technical Analysis
* **Extended ACL Configuration:** Designed and verified rule-sets on Cisco routing interfaces to control packet flow based on source/destination IP, protocol (TCP/UDP), and port numbers.
* **Traffic Filtering Logic:** Verified ACL effectiveness in restricting unauthorized traffic while maintaining availability for essential services.
* **Validation:** Used active connectivity testing to confirm that security policies directly impact packet pathing.
* **Deliverable:** [Extended ACLs Lab](./Configuring%20and%20Verifying%20Extended%20ACLs.pdf)

---

## 3. CIS Controls & Defensive Hardening
### Overview
Analysis of network-level security through the lens of CIS Controls v8, focusing on hardening perimeter devices and detecting unauthorized traffic patterns.

### Technical Analysis
* **Hardening Tactics:** Configuration of routers, firewalls, and switches to disable unnecessary services and close exposed ports (CIS Control 4.1).
* **Threat Modeling:** Analysis of infrastructure exposure to *Sniffing* and *Man-in-the-Middle (MITM)* attacks.
* **Defensive Layers:** Implementation of SIEM-like auditing to centralize log analysis and facilitate real-time incident response.
* **Deliverable:** [CIS Controls & Hardening Debate](./Debate%20Académico%202.pdf)

---

## Engineering Takeaways
1. **Perimeter Defense is Insufficient:** Modern networks require internal segmentation. Relying on firewalls alone permits lateral movement once the perimeter is breached.
2. **Granular ACLs:** Security policies must be as specific as possible. Broad rules (e.g., `permit ip any any`) are the primary cause of network vulnerabilities.
3. **Continuous Validation:** Implementing security controls is only half the battle; constant auditing (using CIS benchmarks and log monitoring) is required to ensure policies remain effective against evolving threats.
