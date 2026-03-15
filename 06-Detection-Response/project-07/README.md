# Project 7: Intrusion Detection with Suricata 🛡️🔍

## Project Overview
In this project, I acted as a security analyst responsible for monitoring network traffic using **Suricata**, an open-source Intrusion Detection System (IDS). I moved beyond manual packet inspection to automated alerting by writing and testing custom signatures. I analyzed the two primary types of Suricata logs: the simplified `fast.log` and the highly detailed, JSON-formatted `eve.json`.

## Technical Skills & Tools
* **IDS Configuration:** Writing custom rules with specific actions, headers, and options.
* **Log Analysis:** Parsing network telemetry using the `jq` command-line processor.
* **Signature Syntax:** Understanding the `Action`, `Header`, and `Rule Options` (msg, flow, content, sid, rev).
* **Traffic Simulation:** Running Suricata against `.pcap` files to validate rule efficacy.



## Technical Tasks & Findings

### 1. Anatomy of a Custom Rule
I analyzed a signature designed to detect HTTP GET requests:
`alert http $HOME_NET any -> $EXTERNAL_NET any (msg:"GET on wire"; flow:established,to_server; content:"GET"; http_method; sid:12345; rev:3;)`
* **Action:** `alert` (triggers a log entry).
* **Protocol:** `http`.
* **Flow:** `established,to_server` (targets traffic from the client to the server).
* **Payload Match:** Looks for the string `"GET"` specifically within the `http_method`.

### 2. Triggering Alerts
I executed Suricata in a Linux environment to process a sample packet capture:
* **Command:** `sudo suricata -r sample.pcap -S custom.rules -k none`
* **Verification:** I monitored the `/var/log/suricata/` directory to ensure `fast.log` and `eve.json` were generated correctly.



### 3. Advanced Telemetry Parsing with jq
While `fast.log` provided quick alert summaries, I used the `jq` tool to extract specific forensic data from the `eve.json` file.
* **Command:** `jq 'select(.event_type=="alert") | [.timestamp, .flow_id, .alert.signature, .proto, .dest_ip]' /var/log/suricata/eve.json`
* **Key Discovery:** I identified a specific flow (Flow ID: `142.250.1.102`) that triggered a "GET on wire" alert with a **Severity Level 3**. 

## Key Takeaway
Suricata is a powerful force multiplier for a SOC. By mastering rule syntax and JSON log parsing, I can correlate different events using a shared `flow_id`, allowing me to track an attacker's entire conversation across a network rather than just seeing isolated packets.

---
### 📑 Artifacts
* **Tools:** Suricata IDS, Bash, jq.
* **Data Sources:** `sample.pcap`, `custom.rules`.
* **Log Outputs:** `fast.log`, `eve.json`.
