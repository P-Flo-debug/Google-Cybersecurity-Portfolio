# Lab: Network Hardening & Risk Assessment

## 🎯 Incident Overview
Following a major data breach that compromised customer names and addresses, I conducted a risk assessment to identify network vulnerabilities. The goal was to implement strong, consistent hardening practices to prevent future unauthorized access.

## 🔍 Vulnerability Analysis
The inspection revealed four critical security gaps:
* **Password Hygiene:** Employees were discovered sharing passwords.
* **Default Credentials:** The database administrative password was left at factory defaults.
* **Firewall Gaps:** Rules were not in place to filter incoming and outgoing traffic.
* **Lack of MFA:** Multi-factor authentication was not utilized for sensitive accounts.

## 🛠️ Proposed Hardening Solutions
Based on the assessment, I recommended the following three primary hardening methods:

### 1. Multi-Factor Authentication (MFA)
Implementing MFA adds a layer of security beyond a password, such as fingerprint scans or one-time passcodes. This significantly reduces the likelihood of successful brute force attacks and makes password sharing less effective.

### 2. Strong Password Policies
I proposed refined policies that include:
* Enforcing minimum password lengths (15+ characters) and complexity.
* Prohibiting the reuse of old or default passwords.
* Implementing account lockout rules (e.g., suspending access after five unsuccessful attempts).

### 3. Regular Firewall Maintenance
Firewall maintenance ensures that security configurations stay ahead of evolving threats. Administrators must regularly update rules to reflect current standards for allowed and denied traffic, specifically placing suspicious sources on a denied traffic list.
