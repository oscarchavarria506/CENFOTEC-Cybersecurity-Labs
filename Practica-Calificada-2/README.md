# Cloud Network Security and Traffic Mitigation Lab (Azure NSG)

## Project Overview
This repository documents hands-on cloud security engineering exercises focused on network infrastructure protection within Microsoft Azure. The project involves configuring Network Security Groups (NSGs) and leveraging Azure Network Watcher to analyze packet flow, enforce network segmentation, and mitigate multi-vector cyber attacks in a multi-subnet virtual network environment.

## Technologies & Tools Used
* **Cloud Infrastructure:** Microsoft Azure Virtual Networks (VNet)
* **Traffic Control & Firewalls:** Network Security Groups (NSGs) & Security Rules
* **Network Diagnostics:** Azure Network Watcher (Connectivity Check, IP Flow Verify)
* **Network Architecture:** CIDR Subnetting (10.0.1.0/24 infrastructure)

---

## Lab Execution & Technical Logic

### Phase 1: Connectivity Diagnostics and Security Verification
* **Network Topology Validation:** Conducted diagnostic connectivity verification across isolated subnets within the virtual network using Azure Network Watcher.
* **Inbound/Outbound Evaluation:** Verified transport layer traffic flow state against active security groups, achieving verified low-latency routing across localized subnets.

### Phase 2: Threat Mitigation & Security Policy Hardening

#### 1. Remote Desktop Protocol (RDP) Brute-Force Mitigation
* **Threat Scenario:** External threat actors executing automated brute-force discovery attacks targeting open RDP interfaces (Port 3389).
* **Mitigation Strategy:** Enforced an explicit inbound security rule targeting the "Internet" service tag. Applied a high-priority "Deny" action to intercept and drop unauthorized external connection requests before reaching the target VM infrastructure.

#### 2. DDoS Attack Vector Abatement
* **Threat Scenario:** Inbound Distributed Denial of Service (DDoS) attempt originating from a specific high-risk malicious IP address (103.113.68.12) targeting the enterprise application server (Port 80).
* **Mitigation Strategy:** Provisioned an explicit inbound firewall rule to filter out all traffic from the hostile remote IP. Successfully validated absolute mitigation via IP Flow Verify while confirming uninterrupted public web access from legitimate remote systems.

#### 3. Lateral Movement Prevention (Network Segmentation)
* **Threat Scenario:** Post-compromise scenario where an attacker controls an asset inside Subnet 0 (10.0.0.0/24) and attempts network-wide lateral exploration to compromise internal staging subnets.
* **Mitigation Strategy:** Implemented a granular zero-trust boundary by creating a rule that denies all incoming traffic originating from the compromised subnet. Verified that intra-subnet communications within production zones remained secure and unaffected.

#### 4. Data Exfiltration Prevention (Outbound Control)
* **Threat Scenario:** A compromised active instance attempting unauthorized outbound data transmission (exfiltration) to an external rogue command-and-control server (175.45.176.37).
* **Mitigation Strategy:** Engineered a custom outbound security rule restricting all egress traffic destined for the unauthorized external endpoint. Validated strict traffic drop execution while ensuring compliant business-critical outbound web flows remained open.

---

## Key Security Takeaways
1. **The Core of Micro-segmentation:** Restricting inter-subnet traversal blocks lateral infection paths, effectively containing potential network breaches to their initial point of entry.
2. **Egress Filtering Importance:** Perimeter defense is incomplete without strict outbound monitoring. Implementing outbound NSG controls is a crucial layer to disrupt data exfiltration and control-and-command synchronization.
