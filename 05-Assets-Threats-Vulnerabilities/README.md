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

### 2. Banking Sector Risk Register & Assessment
**Goal:** Analyze a financial institution's operational environment to quantify and prioritize security risks to critical assets.

* **Scenario:** A coastal bank with 120 employees (remote and on-premise) and 2,200 accounts, requiring strict compliance with Federal Reserve regulations.
* **Skills Applied:** Risk Quantification ($Likelihood \times Severity$), Business Impact Analysis (BIA), Regulatory Compliance.
* **Methodology:** * Conducted a threat assessment of the bank's **Funds** asset.
    * Calculated priority scores to rank threats ranging from environmental disasters to cyber-attacks.
    * Analyzed how the "human element" (120 data handlers) impacts the organization's attack surface.
* **Key Findings:** * **Critical Risks (Score 9):** Identified **Business Email Compromise (BEC)** and **Poor Encryption** as the highest priority threats.
    * **Strategic Insight:** While physical crime is low in the coastal area, the high volume of employees creates a significant risk of social engineering. Furthermore, environmental factors introduce supply chain risks that could impact daily cash availability requirements.

**[View Risk Register Spreadsheet](./Risk-register.csv)**

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
