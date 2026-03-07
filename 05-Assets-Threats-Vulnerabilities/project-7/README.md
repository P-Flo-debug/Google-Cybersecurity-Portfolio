# Project 7: Social Engineering & USB Baiting Analysis 🔌🩹

## Project Overview
In this project, I analyzed a "USB Baiting" scenario—a social engineering attack where a physical device is left in a public place to trick employees into plugging it into a secure network. I evaluated the contents of a found drive to determine the potential impact on both the individual (Jorge) and the organization (the hospital).

## Technical Skills & Tools
* **Social Engineering Analysis:** Recognizing "Baiting" and "Quid Pro Quo" tactics.
* **Risk Assessment:** Evaluating the exposure of Personally Identifiable Information (PII) and Sensitive PII (SPII).
* **Defense in Depth:** Categorizing mitigations into Technical, Operational, and Managerial controls.
* **Attacker Mindset:** Anticipating how a threat actor uses reconnaissance data for impersonation and lateral movement.



## Analysis Summary

### 1. Data Sensitivity & Contents
The drive contained a high-risk mixture of personal and professional files:
* **Personal:** Wedding plans and vacation photos (used for social engineering/phishing).
* **Professional:** Employee budget information and shift schedules (SPII that could lead to financial fraud or physical security breaches).

### 2. Attacker Mindset
I identified that an attacker would use this data for **Reconnaissance**. By knowing Jorge’s wedding plans and team budget, an attacker could craft a highly convincing **Spear Phishing** email or impersonate Jorge to manipulate hospital business practices.

### 3. Mitigation Strategy (Defense in Depth)
To protect the hospital, I recommended a three-tiered control approach:

| Control Type | Recommendation |
| :--- | :--- |
| **Technical** | Disable **Auto-Run/Auto-Play** on all endpoints to prevent automatic malware execution. |
| **Operational** | Implement routine vulnerability scans and enforce the use of encrypted, company-issued encrypted drives only. |
| **Managerial** | Conduct **Security Awareness Training** specifically regarding the dangers of found removable media. |



## Key Takeaway
"The human is the weakest link." This lab highlights that even with the best firewalls, one curious employee plugging in a found USB drive can bypass an entire security stack. Promoting a culture of "Zero Trust" regarding external hardware is essential for organizational safety.

---
### 📑 Artifacts
* [View USB Risk Analysis Worksheet](./Parking-lot-USB-exercise.pdf)
