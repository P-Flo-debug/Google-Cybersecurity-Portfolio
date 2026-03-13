# Project 3: Command-Line Packet Capture with tcpdump 🐧📡

## Project Overview
In this project, I used **tcpdump**, a powerful command-line packet analyzer, to capture and filter network traffic on a Linux-based virtual machine. Unlike GUI-based tools, `tcpdump` is essential for analyzing traffic on remote servers and embedded systems. I focused on identifying network interfaces, capturing specific protocol traffic, and saving data for later forensic review.

## Technical Skills & Tools
* **Network Interface Management:** Using `ifconfig` and `tcpdump -D` to map hardware interfaces (e.g., `eth0`).
* **Traffic Capture:** Utilizing the `-i`, `-v`, and `-c` flags to stream live packet data.
* **Forensic Storage:** Writing traffic to persistent files using the `-w` (write) and `-r` (read) flags.
* **Payload Inspection:** Using the `-X` flag to visualize data in **Hexadecimal** and **ASCII** formats.



## Investigation & Technical Tasks

### 1. Interface Identification
I began by identifying the active network interfaces available for monitoring.
* **Command:** `sudo tcpdump -D`
* **Result:** Identified `eth0` as the primary Ethernet interface for live capture.

### 2. Live Traffic Inspection
I performed a verbose capture to analyze the metadata of the first 5 packets passing through the system.
* **Command:** `sudo tcpdump -i eth0 -v -c5`
* **Observations:** Identified IP packet fields including **TOS (Type of Service)**, **TTL (Time to Live)**, and **TCP sequence/acknowledgment numbers**.

### 3. Background Capture & Port Filtering
To simulate an investigation into web traffic, I ran a filtered capture in the background while generating traffic via `curl`.
* **Command:** `sudo tcpdump -i eth0 -nn -c9 port 80 -w capture.pcap &`
* **Purpose:** The `-nn` flag was used to disable name lookups, a security best practice that prevents alerting potential threat actors during an investigation.



### 4. Forensic Read & Hex Analysis
I reviewed the saved `capture.pcap` file to look for anomalies in the packet payloads.
* **Command:** `sudo tcpdump -nn -r capture.pcap -X`
* **Insight:** The `-X` flag allowed me to see the raw data within the packets. This is a critical step for identifying hidden malware signatures or unauthorized text-based data exfiltration.

## Key Takeaway
Mastering `tcpdump` allows for surgical precision in network monitoring. By filtering specifically by port and interface, I can capture exactly the data I need without overwhelming the system's resources, making it a primary tool for real-time incident response.

---
### 📑 Artifacts
* **Environment:** Linux Bash Terminal.
* **Captured File:** `capture.pcap` (TCP Port 80 traffic).
