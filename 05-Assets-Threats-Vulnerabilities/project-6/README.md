# Project 6: Access Control & IAM Analysis 🔐

## Project Overview
In this scenario, I acted as the first cybersecurity professional for a growing business. After a suspicious payroll deposit was made to an unknown account, I conducted a forensic analysis of the system's access logs and employee directory to identify the security gaps that allowed the breach to occur.

## Technical Skills & Tools
* **Log Analysis:** Reviewing event logs to track user activity, IP addresses, and timestamps.
* **Identity & Access Management (IAM):** Assessing the lifecycle of employee accounts and permissions.
* **AAA Framework:** Evaluating Authentication, Authorization, and Accounting controls.
* **Threat Identification:** Recognizing unauthorized access from stale or over-privileged accounts.

## Step-by-Step Execution

### 1. Incident Investigation (The Event Log)
I analyzed the system event logs to pinpoint the exact moment of the unauthorized transaction.
* **User Involved:** `Legal\Administrator`
* **Date/Time:** 10/03/2023 at 8:29:57 AM
* **Source IP:** 152.207.255.255
* **Action:** Unauthorized payroll event added.

### 2. Identifying the Root Cause (Cross-Referencing)
By comparing the event log with the **Employee Directory**, I identified two major access control failures:
* **Privilege Creep:** The `Legal` account had `Administrator` privileges that were unnecessary for its role.
* **Stale Accounts:** The audit revealed that accounts (such as a former contractor) remained active with administrative access long after their contract ended (e.g., Robert Taylor Jr., whose contract ended in 2019 but was used for the 2023 breach).

### 3. Mitigation Recommendations
To prevent future incidents, I proposed the following security enhancements:
* **Implement IAM Policies:** Establish a formal process for onboarding and offboarding employees to ensure access is revoked immediately upon termination.
* **Enforce the Principle of Least Privilege (PoLP):** Transition from a "shared admin" model to role-specific permissions, ensuring the Legal department no longer has payroll or administrative rights.
* **Multi-Factor Authentication (MFA):** Deploy MFA across all administrative accounts to prevent unauthorized login even if credentials are compromised.

## Key Takeaway
This project highlights that **technical tools are only as effective as the policies governing them.** A lack of account accountability is a high-risk vulnerability that can lead to significant financial loss.

---
### 📑 Project Evidence & Analysis
To conduct this audit, I cross-referenced the raw system logs against the internal personnel directory:

* [View Incident Event Log](./Accounting-exercise-Event-log.csv) — Contains the specific timestamp, IP address, and unauthorized payroll action.
* [View Employee Directory](./Accounting-exercise-Employee-directory.csv) — Used to identify the threat actor by matching IP addresses and contract end dates.
* [View Completed Access Control Worksheet](./Access-control-worksheet.pdf) — My final analysis and mitigation report.
