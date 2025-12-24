# Lab: OS Hardening & Brute Force Mitigation

## 🎯 Incident Overview
A former employee performed a **brute force attack** to gain access to a web host's admin panel by guessing a **default password**. They modified the site's source code to redirect users to a malicious URL (`greatrecipesforme.com`).

## 🔍 Findings
* **Protocol Analysis:** I used **tcpdump** to track the redirection from legitimate DNS/HTTP requests to the malicious ones.
* **Hardening Gaps:** The admin password was left as the default, and there were no lockout policies in place.

## 💡 Recommendations
* **Secure Password Policy:** Remove all default passwords.
* **Account Lockout:** Implement a policy to lock accounts after multiple failed login attempts.
* **MFA:** Require Multi-Factor Authentication for administrative access.
