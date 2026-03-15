# Course 6: Detect and Respond 🚨🛡️

## Course Overview
This module focuses on the operational side of cybersecurity: the **Security Operations Center (SOC)**. In this course, I transitioned from planning and prevention to active monitoring, incident detection, and response. I gained hands-on experience with SIEM tools, network traffic analysis, and the NIST Incident Response lifecycle to manage and mitigate active security threats.

## 🛠️ Detection & Response Toolkit
* **SIEM Tools:** [To be added: e.g., Chronicle, Splunk]
* **Network Analysis:** [To be added: e.g., Wireshark, tcpdump]
* **Intrusion Detection (IDS):** [To be added: e.g., Snort, Suricata]
* **Frameworks:** NIST SP 800-61 (Incident Handling), VERIS Schema.



---

## 📑 Featured Projects

### 🚀 Project 1: Ransomware Incident Documentation
* **Goal:** Document a high-impact ransomware attack at a healthcare clinic using an Incident Handler's Journal.
* **Outcome:** Analyzed the attack vector (Spear Phishing) and categorized the breach details using the 5 W's to assist in the forensic recovery process.
* **Skills:** `Incident Documentation` `Phishing Analysis` `Ransomware Awareness`
* **[View Project Details](./project-01)**

### 🚀 Project 2: Network Traffic Analysis with Wireshark
* **Goal:** Use Wireshark to intercept and analyze a packet capture (.pcap) file to identify suspicious network behavior.
* **Outcome:** Successfully filtered traffic by IP, MAC address, and Port; analyzed the TCP/IP layers; and inspected DNS queries and TCP payloads.
* **Skills:** `Packet Analysis` `Wireshark` `Network Protocols (TCP/UDP/ICMP/DNS)`
* **[View Project Details](./project-02)**

### 🚀 Project 3: Command-Line Packet Capture with tcpdump
* **Goal:** Identify network interfaces and capture live traffic on a Linux VM using the `tcpdump` utility.
* **Outcome:** Captured port 80 traffic into a `.pcap` file, filtered packets using command-line flags, and inspected hexadecimal/ASCII payloads for forensic analysis.
* **Skills:** `Linux CLI` `tcpdump` `Packet Sniffing` `Network Forensics`
* **[View Project Details](./project-03)**

### 🚀 Project 4: Comparative Analysis - Wireshark vs. tcpdump
* **Goal:** Research and document the technical similarities and distinct use cases for GUI-based and CLI-based network protocol analyzers.
* **Outcome:** Created a technical comparison chart identifying key differences in interface, resource consumption, and forensic capabilities.
* **Skills:** `Tool Evaluation` `Network Forensics` `Technical Documentation`
* **[View Project Details](./project-04)**

### 🚀 Project 5: Threat Intelligence & The Pyramid of Pain
* **Goal:** Use VirusTotal to analyze a malicious file hash and map associated Indicators of Compromise (IoCs) to the Pyramid of Pain framework.
* **Outcome:** Identified the "Flagpro" malware and linked the attack to the "BlackTech" APT group. Documented IPs, domains, and TTPs to increase the cost of future attacks for the adversary.
* **Skills:** `Threat Intelligence` `VirusTotal` `OSINT` `Pyramid of Pain` `MITRE ATT&CK`
* **[View Project Details](./project-05)**

### 🚀 Project 6: Incident Response Playbook & Ticket Resolution
* **Goal:** Resolve a verified phishing alert by following a standardized Phishing Playbook and flowchart.
* **Outcome:** Evaluated email artifacts (headers, body, and attachments), performed an escalation based on alert severity, and documented the resolution in a professional ticket format.
* **Skills:** `Incident Handling` `Playbook Execution` `Ticket Documentation` `Phishing Analysis`
* **[View Project Details](./project-06)**

### 🚀 Project 7: Intrusion Detection with Suricata
* **Goal:** Configure Suricata IDS to monitor network traffic using custom rules and analyze generated telemetry logs.
* **Outcome:** Successfully triggered alerts using a custom signature, analyzed `fast.log` for quick alerts, and utilized `jq` to parse complex `eve.json` telemetry for deep-dive investigation.
* **Skills:** `Intrusion Detection (IDS)` `Suricata` `Rule Writing` `JSON Parsing (jq)` `Network Telemetry`
* **[View Project Details](./project-07)**

*(More projects will be added as they are completed)*

---

## 📈 Key Learning Objectives
* Analyzing network packets to identify signs of intrusion.
* Configuring and monitoring Security Information and Event Management (SIEM) alerts.
* Documenting incident timelines and "Lessons Learned" reports.
* Categorizing security events using industry-standard schemas.
