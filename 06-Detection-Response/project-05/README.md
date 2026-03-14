# Project 5: Threat Intelligence & The Pyramid of Pain 🛡️🔺

## Project Overview
In this project, I acted as a Level 1 SOC Analyst investigating a suspicious file download alert at a financial services company. After retrieving the SHA256 hash of a password-protected spreadsheet, I used **VirusTotal** to conduct OSINT (Open Source Intelligence) research. I mapped my findings to the **Pyramid of Pain** to determine the severity of the threat and the difficulty of remediating the indicators.

## Technical Skills & Tools
* **Threat Intelligence Platform:** VirusTotal.
* **Malware Classification:** Identifying families (e.g., Flagpro) and threat actors (e.g., BlackTech).
* **IoC Management:** Extracting IPs, domains, and hashes.
* **Framework Application:** Utilizing the Pyramid of Pain and MITRE ATT&CK® TTPs.



## The Investigation: Flagpro Malware
### 1. VirusTotal Verdict
* **Detection Ratio:** 50+ security vendors flagged the hash as malicious.
* **Community Score:** -291 (highly malicious).
* **Attribution:** The investigation identified the malware as **Flagpro**, a tool used by the advanced threat actor group **BlackTech** (an APT group based in China).

### 2. The Pyramid of Pain Breakdown
I documented the following Indicators of Compromise (IoCs) to help the security team block the attack:

| Level | Indicator Type | Value/Detail |
| :--- | :--- | :--- |
| **Tough!** | **TTPs** | Command and Control (C2) behavior |
| **Challenging** | **Tools** | Input Capture (Credential stealing) |
| **Annoying** | **Network Artifacts** | Malicious HTTP Requests |
| **Simple** | **Domain Names** | `a.sinkhole.yourtrap.com` |
| **Easy** | **IP Addresses** | `114.149.208.238` |
| **Trivial** | **Hash Values (MD5)** | `287d612e29b71c90aa54947313810a25` |

## Incident Timeline
* **1:11 p.m.:** Employee receives a spear-phishing email with a password-protected attachment.
* **1:13 p.m.:** File downloaded and decrypted by the user.
* **1:15 p.m.:** Payload executes, creating unauthorized executable files.
* **1:20 p.m.:** IDS detects the activity and alerts the SOC.

## Key Takeaway
By documenting the TTPs and Tools used by BlackTech, we move beyond just blocking "trivial" hashes and start making it much harder for the attacker to maintain their foothold. This analysis provides the intelligence needed to pivot from a reactive posture to a proactive defense.

---
### 📑 Artifacts
* [Pyramid of Pain Worksheet](./Pyramid-of-Pain.pdf)
* [Incident Handler Journal Entry #02](./journal-02.pdf)
