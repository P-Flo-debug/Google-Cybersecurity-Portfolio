# Case Study: Internal IT Audit - Botium Toys

## 🎯 Project Overview
I conducted an internal IT audit for **Botium Toys**, a growing retail company. The audit's goal was to evaluate the current security posture, identify risks to critical assets, and ensure compliance with **PCI DSS** and **GDPR**.

## 📋 Audit Findings: Controls Assessment
Using the **NIST Cybersecurity Framework (CSF)**, I identified several critical gaps in the company's existing controls:

| Control Name | Status | Purpose & Finding |
| :--- | :--- | :--- |
| **Least Privilege** | ❌ No | All employees currently have access to sensitive customer data. |
| **Encryption** | ❌ No | Financial data and PII are stored in plaintext, risking a breach of confidentiality. |
| **IDS** | ❌ No | There is no system to detect anomalous traffic or potential intrusions. |
| **Disaster Recovery** | ❌ No | No plans or backups exist, threatening business continuity. |
| **Firewall** | ✅ Yes | Correctly configured to block unwanted traffic. |
| **Physical Security** | ✅ Yes | Sufficient locks, CCTV, and fire prevention are in place. |



## ⚖️ Compliance Checklist
* **PCI DSS:** Non-compliant. Credit card information is not encrypted and is accessible to all employees.
* **GDPR:** Non-compliant. While a 72-hour breach notification plan exists, data is not classified or encrypted.
* **SOC (Type 1 & 2):** Non-compliant. User access policies are not established, and sensitive data is not private.

## 💡 Top Recommendations
To reduce the high risk score of **8/10**, the following fixes are top priority:
1. **Enforce Least Privilege:** Restrict data access to only those who need it for their job.
2. **Implement Encryption:** Secure all customer PII and financial data at rest and in transit.
3. **Establish Password Policies:** Deploy a centralized password manager to enforce complexity requirements.
4. **Deploy an IDS:** Monitor the network for unauthorized access or malicious signatures.
