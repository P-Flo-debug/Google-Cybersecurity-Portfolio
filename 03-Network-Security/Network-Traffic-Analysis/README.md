# Lab: Network Traffic Analysis & DNS Troubleshooting

## 🎯 Incident Overview
A handful of customers reported they were unable to access the company website, receiving a "destination port unreachable" error. As a cybersecurity analyst, I utilized **tcpdump** to capture network traffic and investigate the connection failure between the browser and the DNS server.



## 🔍 Technical Log Analysis
By inspecting the `tcpdump` log (captured at **13:24:32**), the following sequence was identified:

1.  **The Request:** The browser used the **UDP protocol** to send a query to the DNS server at `203.0.113.2` on **Port 53** to retrieve the IP address for `yummyrecipesforme.com`.
2.  **Flags:** The query included a `35084+ A?` flag, which indicates a standard request for an **A record** (mapping a domain name to an IP address).
3.  **Error Response:** The DNS server responded with an **ICMP packet** containing the error message: `udp port 53 unreachable`.
4.  **Conclusion:** Because Port 53 is the standard port for DNS service, its "unreachable" status confirmed that the DNS server was not responding to legitimate traffic.

## 🛠️ Root Cause & Next Steps
Based on the analysis, there are two suspected root causes for this incident:
* **DoS Attack:** The DNS server may have been disabled by a flood of information, making it unable to respond.
* **Firewall Misconfiguration:** A change in the firewall settings may be blocking all network traffic on Port 53.

**Next Steps for the Technical Team:**
* Verify the functional status of the DNS server.
* Audit firewall configurations to ensure Port 53 is not being unintentionally blocked.

## 🧠 Tools & Protocols Applied
* **tcpdump:** Network analyzer used for packet sniffing and traffic capture.
* **UDP (User Datagram Protocol):** The connectionless transport protocol used for the DNS query.
* **ICMP (Internet Control Message Protocol):** The network layer protocol used to return the error message.
* **DNS (Port 53):** The application-layer service that failed to resolve the domain.
