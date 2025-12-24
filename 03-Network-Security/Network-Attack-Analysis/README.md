# Lab: Analyzing Network Attacks (TCP SYN Flood)

## 🎯 Incident Overview
I investigated a "connection timeout" error on a company web server. Using a packet sniffer, I identified a large volume of **TCP SYN** requests originating from an unfamiliar IP address.

## 🔍 Attack Mechanics
* **Type:** TCP SYN Flood (Denial of Service).
* **Technique:** The attacker sent a massive volume of SYN requests but never completed the three-way handshake, exhausting the server's ability to respond to legitimate users.



## 🛠️ Mitigation
* **Isolation:** Temporarily took the server offline to recover.
* **Filtering:** Configured the firewall to block the malicious source IP address.
