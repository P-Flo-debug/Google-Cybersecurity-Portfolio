# Lab: Analyzing Network Attacks (TCP SYN Flood)

## 🎯 Incident Overview
I investigated a "connection timeout" error on a company web server. Using a packet sniffer, I identified a large volume of **TCP SYN** requests originating from an unfamiliar IP address, suggesting a **Denial of Service (DoS)** attack.

## 🔍 Technical Analysis: The Three-Way Handshake
A normal connection relies on the **TCP three-way handshake**:
1. **SYN:** The source sends a request to connect.
2. **SYN-ACK:** The destination reserves resources and accepts the request.
3. **ACK:** The source acknowledges and the connection is established.

### Attack Mechanics
In this incident, the logs showed a **SYN Flood** attack. The malicious actor sent a massive number of SYN packets all at once, overwhelming the server’s available resources. Because the server was forced to reserve resources for these incomplete handshakes, no resources were left for legitimate users, resulting in the connection timeout errors.


## 🛠️ Mitigation & Response
To restore service and protect the web server, the following actions were taken:
* **Isolation:** Temporarily took the server offline to clear the backlog of half-open connections and recover resources.
* **Firewall Configuration:** Configured the firewall to block the specific malicious source IP address detected in the logs.
* **Reporting:** Documented the root cause as a SYN flood attack to inform long-term defense strategies.
