# Project 6: Incident Response Playbook & Ticket Resolution 🎫🚩

## Project Overview
In this project, I performed the duties of a Level 1 SOC Analyst responding to a verified phishing incident. Using a standardized **Phishing Playbook**, I moved from the initial alert evaluation to the final ticket escalation. This project demonstrates my ability to work within a structured security team environment and communicate technical findings clearly to higher-level analysts (Level 2/Tier II).

## Technical Skills & Tools
* **Workflow Automation:** Executing steps based on a Phishing Flowchart.
* **Email Header Analysis:** Identifying sender spoofing and suspicious source IPs.
* **Incident Lifecycle:** Transitioning a ticket from "Investigating" to "Escalated."
* **Documentation:** Drafting professional ticket comments that include technical justifications.



## The Playbook Process

### 1. Evaluating the Alert
I analyzed Ticket **A-2703**, which flagged a possible malware download from a phishing attempt. Key indicators found during the evaluation:
* **Sender Inconsistency:** The "From" name (Clyde West) did not match the suspicious domain (`76tguyhh6tgftrt7tg.su`).
* **Source Reputation:** The sender IP `114.114.114.114` was flagged as suspicious.
* **Social Engineering:** The email body contained significant grammatical errors, a common hallmark of phishing.

### 2. Malware Verification
As established in previous investigations, the attachment `bfsvc.exe` (SHA256: `54e6ea47eb04634d3e87fd7787e2136ccfbcc80ade34f246a12cf93bab527f6b`) was already verified as malicious via VirusTotal.



### 3. Escalation & Resolution
Following the playbook's criteria for **Medium Severity** and **Confirmed Malicious Content**, I took the following actions:
* **Status Update:** Moved the ticket status from **Investigating** to **Escalated**.
* **Justification:** Provided a detailed summary in the ticket comments, citing the mismatching sender identity, the malicious file hash, and the failed integrity of the email content.

## Key Takeaway
Consistency is the key to effective security operations. By following a playbook, I ensured that every piece of evidence—from the sender's IP to the file's hash—was analyzed before escalating. This prevents "investigation sprawl" and ensures that Level 2 analysts have all the necessary context to begin remediation immediately.

---
### 📑 Artifacts
* [Completed Alert Ticket A-2703](./alert-ticket.pdf)
* [Incident Handler Journal Entry #03](./journal-02.pdf)
