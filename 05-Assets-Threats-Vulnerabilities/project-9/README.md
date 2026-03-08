# Project 9: Spear Phishing & Email Forensic Analysis 📧🕵️‍♂️

## Project Overview
As a security analyst at "Imaginary Bank," I was tasked with investigating a highly targeted spear phishing attempt sent to the CFO. The email used psychological triggers (urgency and authority) to trick the executive into downloading a malicious "collaboration tool" called ExecuTalk. I conducted a forensic review of the email's metadata and content to determine its legitimacy.

## Technical Skills & Tools
* **Phishing Analysis:** Identifying social engineering tactics (Sense of Urgency, Authority).
* **Email Header Forensics:** Inspecting sender domains, Reply-To addresses, and timestamps.
* **Link Analysis:** Safely inspecting URLs for credential harvesting forms.
* **Remediation:** Implementing "Quarantine" procedures for malicious internal communications.



## Forensic Investigation Findings

### 1. Header Analysis
I identified several "red flags" in the email header that immediately signaled a threat:
* **Domain Mismatch:** The sender used `imaginarybank@gmail.org` instead of the official company domain (`@imaginarybank.com`).
* **Subject Line Manipulation:** The subject began with `RE:`, a common tactic to trick the recipient into thinking the email is part of an ongoing, trusted conversation.
* **Spelling Errors:** The subject line contained a glaring typo: `ecsecutiv's`.

### 2. Body & Social Engineering Tactics
The threat actor used "Brand Imitation" to appear legitimate, including:
* **Fake Branding:** Use of trademark and copyright symbols (©, ®) for "ExecuTalk."
* **Platform Spoofing:** Offering downloads for Mac, Windows, and Android to build trust.
* **Induced Urgency:** Stating the invitation "will expire in 48 hours" to pressure the CFO into acting without thinking.



### 3. URL & Landing Page Audit
I analyzed the redirect linked to the "Download" buttons. 
* **The Clue:** The landing page was a replica login form.
* **The Verdict:** The URL did not match the official organization domain or a trusted SaaS provider. This confirmed the page was a **Credential Harvester** designed to steal the CFO's bank credentials.

## Final Recommendation: QUARANTINE
Based on the evidence of domain spoofing, spelling errors, and malicious URLs, I classified this email as a **Spear Phishing attack**. I recommended:
1. **Quarantining** the email from all user inboxes.
2. **Blacklisting** the sender domain `@gmail.org` at the mail gateway.
3. **Internal Alerting** to warn other executives of the ongoing "ExecuTalk" campaign.

---
### 📑 Artifacts
* [View Phishing Analysis Report](./Phishing-Analysis-Report.md)
