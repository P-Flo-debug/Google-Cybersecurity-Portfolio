# Lab: OS Hardening & Brute Force Investigation (yummyrecipesforme.com)

## 🎯 Incident Overview
I investigated a security compromise of the cooking website `yummyrecipesforme.com`. A malicious actor gained administrative access via a **brute force attack**, modified the site's source code with a JavaScript function, and redirected users to a malware-hosting site (`greatrecipesforme.com`).

## 🔍 Technical Analysis & Attack Lifecycle
The investigation, conducted in a **sandbox environment** using **tcpdump**, revealed the following attack stages:

1.  **Initial Access:** The attacker correctly guessed the administrative password because it was still set to the **factory default**.
2.  **Unauthorized Modification:** The attacker embedded a JavaScript function in the source code that prompted users to download a "browser update" (malicious executable).
3.  **Malware Delivery (HTTP):** The browser initiated an **HTTP request** at the application layer to download the malicious file once the connection was established.
4.  **Redirection:** After the file was executed, the browser sent a new DNS request for `greatrecipesforme.com` and redirected the user via **HTTP** to the fake website.



## 🛠️ Documented Protocols
* **HTTP (Hypertext Transfer Protocol):** The primary protocol used to transport the malicious file to users' computers and load the fake website.
* **DNS (Domain Name System):** Used to resolve both the legitimate and malicious URLs into IP addresses during the redirection process.

## 💡 Recommended Remediations
To prevent future brute force attacks, I recommend the following OS hardening measures:
* **Password Complexity & History:** Implement a policy requiring passwords of at least **15 characters** and disallow the reuse of previous or **default passwords**.
* **Two-Factor Authentication (2FA):** Require a one-time passcode (OTP) via email or phone, ensuring that a stolen password alone is insufficient for access.
