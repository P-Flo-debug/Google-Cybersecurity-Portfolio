# Project 8: Vulnerability Assessment & Risk Quantification 🛡️📊

## Project Overview
In this project, I conducted a formal vulnerability assessment for a small business's database server. The system hosts critical customer data (PII/SPII) and is public-facing, making it a high-value target. Using the **NIST SP 800-30** risk management framework, I identified potential threats, quantified their impact, and proposed a technical remediation roadmap.

## Technical Skills & Tools
* **Risk Management Frameworks:** NIST SP 800-30 Rev. 1.
* **Risk Quantification:** Calculating risk scores (Likelihood × Severity).
* **Network Security:** Evaluating TLS/SSL, IP Allow-listing, and Database Security.
* **Compliance Knowledge:** Understanding the impact of PCI-DSS and data privacy laws.



## Assessment Components

### 1. Scope & Purpose
The assessment focused on a Linux-based MySQL server (128GB RAM) used for customer data storage. The goal was to identify vulnerabilities that could lead to data exfiltration, unauthorized modification, or Denial of Service (DoS) attacks.

### 2. Risk Assessment Matrix
I evaluated three primary threat sources: Advanced Persistent Threats (APTs), Hackers, and Insider Threats. By scoring each on a scale of 1-3, I identified that all three represented a **Level 9 (High)** risk to the organization.

| Threat Source | Threat Event | Likelihood | Severity | Risk Score |
| :--- | :--- | :---: | :---: | :---: |
| **APT** | Data Exfiltration | 3 | 3 | **9** |
| **Hacker** | Data Alteration/Deletion | 3 | 3 | **9** |
| **Employee** | Reconnaissance/Surveillance| 3 | 3 | **9** |



[Image of a risk assessment matrix showing likelihood vs impact]


### 3. Remediation Strategy
To mitigate the identified risks, I proposed the following technical and administrative controls:
* **Encryption:** Deprecating SSL in favor of **TLS** for all data in transit.
* **Access Control:** Implementing **Multi-Factor Authentication (MFA)** and **Role-Based Access Control (RBAC)**.
* **Network Hardening:** Implementing **IP Allow-listing** to restrict database access to known corporate office IPs only.
* **Integrity:** Utilizing MySQL auditing mechanisms to track and log all data access.

## Key Takeaway
Vulnerability assessments are not just about finding bugs; they are about **prioritization**. By quantifying risk, I can demonstrate to business owners exactly where their resources should be spent to protect their most valuable assets and maintain compliance.

---
### 📑 Artifacts
* [View Full Vulnerability Assessment Report (PDF)](./Vulnerability-assessment-report.pdf)
