# Lab: Network Traffic Analysis (DNS Troubleshooting)

## 🎯 Incident Overview
I acted as a Cybersecurity Analyst to investigate a service disruption where users could not access `www.yummyrecipesforme.com`. I utilized the network analyzer tool **tcpdump** to capture and inspect data packets in transit.

## 🔍 Technical Analysis
By inspecting the `tcpdump` logs, I identified the following sequence:
1.  **Request:** The browser initiated a **UDP** request for an **A record** to the DNS server at `203.0.113.2` on **Port 53**.
2.  **Error:** The server returned an **ICMP** packet with the error: `udp port 53 unreachable`.
3.  **Root Cause:** The DNS server was not listening on Port 53, preventing the domain name from being resolved into an IP address.

## 🛠️ Tools & Protocols Used
* **tcpdump:** Used for packet capture and traffic inspection.
* **DNS (Port 53):** The impacted service.
* **UDP & ICMP:** The transport and network layer protocols analyzed during the investigation.
