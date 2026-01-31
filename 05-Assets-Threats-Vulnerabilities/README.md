# Course 5: Assets, Threats, and Vulnerabilities

## 🛡️ Executive Summary
This repository documents my work on the fifth course of the Google Cybersecurity Professional Certificate. The focus of this module is moving beyond technical tools to master **Risk Management**, **Asset Security**, and the **Attacker Mindset**.

### 🎯 Key Competencies
* **Asset Management:** Cataloging hardware/software and assessing their business value.
* **Risk Classification:** Assigning sensitivity levels based on the CIA Triad (Confidentiality, Integrity, Availability).
* **Threat Modeling:** Applying frameworks like PASTA to anticipate and mitigate attack vectors.
* **Vulnerability Analysis:** Understanding CVEs and prioritizing system patches.

---

## 📁 Featured Projects

### 1. Home Office Asset Inventory & Risk Classification
**Goal:** Identify all devices on a network and classify them based on the risk they pose to the organization if compromised.

* **Project Scope:** Analyzed a small business/home office network consisting of routers, workstations, and IoT devices.
* **Methodology:**
    * Performed an audit of hardware assets and network access patterns.
    * Evaluated the data sensitivity of each device (PII, financial records, system backups).
    * Assigned classification levels: *Public, Internal, Confidential, and Restricted*.
* **Key Outcome:** Identified an **IP Camera** as a high-risk asset. Upgraded its classification to **Confidential** due to the risk of unauthorized PII access and potential for lateral movement within the network.

**[View Project Spreadsheet](./Home-asset-inventory.csv)**

---

### 2. Risk Register: Asset Protection & Threat Analysis

## Project Overview
This project documents a comprehensive risk assessment for a fictional organization's financial assets. By identifying specific threats and vulnerabilities, this register provides a roadmap for prioritizing security controls and mitigation strategies.

## Risk Assessment Framework
The risks identified in the [Risk-register.csv](./Risk-register.csv) are evaluated using a scoring system to determine the **Priority Level**:
* **Likelihood:** The probability of the threat occurring (Scale of 1-3).
* **Severity:** The potential impact on the organization's operations or finances (Scale of 1-3).
* **Priority Score:** Calculated as $Likelihood \times Severity$.

## Executive Summary of Risks
| Asset | Risk | Priority Score |
| :--- | :--- | :--- |
| **Funds** | Business email compromise | **9 (Critical)** |
| **Funds** | Compromised user database | **9 (Critical)** |
| **Funds** | Theft | **6 (High)** |
| **Funds** | Financial records leak | **3 (Medium)** |
| **Funds** | Supply chain disruption | **2 (Low)** |

## Security Observations
The following factors were identified as key drivers for the current risk landscape:
* **Attack Surface:** The organization has a high volume of data handlers (120 employees), which increases the likelihood of social engineering and internal errors.
* **Technical Vulnerabilities:** Key risks include poorly encrypted customer data and publicly accessible backup servers.
* **Operational Environment:** While natural disasters pose a threat to the supply chain, the immediate focus is on mitigating high-priority cyber threats like Business Email Compromise (BEC).

## Mitigation Objectives
The primary goal for the next phase of this project is to implement controls that reduce the "Critical" priority risks, specifically focusing on:
1. **Access Control:** Implementing Multi-Factor Authentication (MFA) to prevent BEC.
2. **Encryption:** Upgrading database encryption standards to protect customer information.
3. **Network Security:** Securing backup servers to prevent unauthorized public access.
---

## 🛠️ Security Frameworks & Concepts
* **NIST Cybersecurity Framework (CSF):** Applied the "Identify" and "Protect" functions.
* **Principle of Least Privilege (PoLP):** Analyzed access levels to minimize exposure.
* **Defense in Depth:** Explored multi-layered security controls to protect high-value assets.

## 🚀 Professional Impact
By completing these activities, I have demonstrated the ability to:
1. Conduct a full asset audit to ensure 100% visibility of a network environment.
2. Communicate technical risks to stakeholders using standardized industry terminology.
3. Prioritize security resources by identifying which assets are most critical to business continuity.

---
*Next Steps: Moving into the Threat Modeling and Vulnerability Assessment modules.*
