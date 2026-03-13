# Project 2: Network Traffic Analysis with Wireshark 🦈💻

## Project Overview
In this project, I performed a deep-dive packet analysis using **Wireshark**, the industry-standard network protocol analyzer. I examined a `.pcap` file containing a web browsing session to identify communication patterns, source/destination signatures, and protocol-specific data. This skill is vital for detecting unauthorized data exfiltration, man-in-the-middle attacks, and malware "beaconing."

## Technical Skills & Tools
* **Protocol Analysis:** Inspecting **TCP**, **UDP**, **ICMP**, **DNS**, and **HTTP** traffic.
* **Display Filters:** Utilizing complex filters (e.g., `ip.addr`, `eth.addr`, `tcp.port == 80`).
* **OSI Model Application:** Deconstructing packets into Frames, Ethernet II, IPv4, and Transport layers.
* **Payload Inspection:** Searching for specific strings (e.g., `curl`) within TCP payloads to identify user-agent activity.



## Investigation Steps & Findings

### 1. Traffic Filtering & Identification
I isolated traffic associated with a specific external server (`142.250.1.139`) to monitor a user's web session. By applying an IP address filter, I reduced thousands of packets down to a manageable set of ICMP and TCP communications.

### 2. DNS Forensic Review
I analyzed DNS traffic on **UDP Port 53** to determine which domains the host was attempting to resolve. 
* **Observation:** The host queried `opensource.google.com`.
* **Resolution:** The DNS "Answers" section provided the associated IP: `142.250.1.139`.



### 3. Packet Layer Deconstruction (OSI Model)
For a selected TCP packet, I analyzed the following metadata:
* **Frame Length:** 54 bytes.
* **TTL (Time to Live):** 64 (indicating a likely Linux/Google-based source).
* **Header Length:** 20 bytes.
* **Flags:** Inspected the TCP handshake flags to verify connection status.

### 4. Payload Analysis
Using the filter `tcp contains "curl"`, I successfully identified that the web request was generated via a command-line tool rather than a standard browser, which is often a sign of automated scripts or potential reconnaissance activity by an attacker.



## Key Takeaway
Network traffic doesn't lie. By mastering Wireshark filters, I can quickly separate legitimate business traffic from suspicious anomalies. Understanding how to read raw packet data is the foundation of effective intrusion detection.

---
### 📑 Artifacts
* **Lab Environment:** Windows VM with Wireshark.
* **Data Source:** `sample.pcap` (Capture file containing web browsing data).
