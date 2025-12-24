# 📑 Incident Report: ICMP Flood DDoS Attack

## 🎯 Incident Summary
The organization experienced a security event where network services suddenly stopped responding due to a **Distributed Denial of Service (DDoS)** attack. The disruption was caused by an incoming flood of **ICMP packets** that overwhelmed the internal network.

## 🛠️ NIST CSF Framework Application

### Identify
A malicious actor targeted the company with an **ICMP flood attack**, affecting the entire internal network. The primary task was identifying all critical network resources that needed to be secured and restored to a functioning state.

### Protect
To mitigate future threats, the cybersecurity team implemented:
* A new firewall rule to **limit the rate** of incoming ICMP packets.
* An **IDS/IPS system** to filter out ICMP traffic based on suspicious characteristics.


### Detect
To improve speed and efficiency in detection, the team configured:
* **Source IP Address Verification:** Checking for spoofed IP addresses on incoming ICMP packets at the firewall.
* **Network Monitoring Software:** Deploying tools to detect abnormal traffic patterns in real-time.

### Respond
In response to the attack, the team blocked the flood and stopped all non-critical services to restore critical functionality. For future events, the team will isolate affected systems, analyze network logs for abnormal activity, and report incidents to upper management.

### Recover
Recovery involved restoring network services to a normal functioning state. In a DDoS scenario, external floods are blocked at the firewall, non-critical services are temporarily stopped to reduce traffic, and critical services are prioritized for restoration. Once the ICMP flood times out, all remaining systems are brought back online.
