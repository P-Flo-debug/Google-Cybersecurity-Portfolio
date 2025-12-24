# 📑 Incident Report: ICMP Flood Denial of Service (DoS)

## 🎯 Incident Summary
The organization experienced a **Denial of Service (DoS)** attack that compromised the internal network for two hours. The attack utilized a flood of **ICMP packets** to overwhelm network resources, causing critical services to stop responding to legitimate traffic.

---

## 🛠️ NIST CSF Analysis

### 1. Identify
* **The Problem:** A malicious actor sent a flood of ICMP pings into the company’s network through an unconfigured firewall.
* **The Vulnerability:** An **unconfigured firewall** allowed the flood of traffic to pass through unchecked.
* **The Risk:** This vulnerability allowed the malicious attacker to overwhelm the network, leading to a loss of availability for critical resources.

### 2. Protect
* **Firewall Hardening:** Implemented a new firewall rule to **limit the rate** of incoming ICMP packets.
* **IP Verification:** Enabled source IP address verification on the firewall to check for and block **spoofed IP addresses**.


### 3. Detect
* **Traffic Monitoring:** Installed network monitoring software to identify and detect abnormal traffic patterns in real-time.
* **Intrusion Prevention:** Deployed an **IDS/IPS system** to filter out suspicious ICMP traffic based on malicious characteristics.

### 4. Respond
* **Containment:** The incident management team responded by blocking incoming ICMP packets immediately to neutralize the flood.
* **Neutralization:** Non-critical network services were taken offline to preserve system stability and allow for investigation.

### 5. Recover
* **Restoration:** Critical network services were restored once the flood was contained and the system was stabilized.
* **Business Continuity:** Affected systems were recovered to normal operation and systems data was validated.
