# Project 8: SIEM Analysis with Wazuh 🖥️📊

## Project Overview
In this project, I acted as a security analyst for an e-commerce store, "Buttercup Games." My objective was to use the **Wazuh SIEM dashboard** to monitor the security health of the organization's infrastructure. I focused on identifying potential brute-force attacks by filtering authentication logs across various web and mail servers.



## Technical Skills & Tools
* **SIEM Operations:** Navigating the Wazuh "Discover" dashboard and managing data indices.
* **Search Syntax:** Using wildcards (`*`), Boolean operators (`AND`, `OR`), and field-specific filtering (e.g., `host.keyword`).
* **Data Correlation:** Analyzing logs from disparate sources (mailsv, www1, vendor_sales) in a single "pane of glass."
* **Security Auditing:** Identifying failed authentication patterns (SSH "root" login failures).

## Investigation Steps & Queries

### 1. Data Ingestion & Initial Discovery
I began by verifying the data set (over 100,000 events) by setting a broad "Absolute" time range to capture all historical logs.
* **Primary Query:** `*`
* **Outcome:** Confirmed data was active for five distinct hosts: `mailsv`, `www1`, `www2`, `www3`, and `vendor_sales`.

### 2. Host-Specific Filtering
To investigate the mail server specifically, I narrowed the telemetry to focus only on the mail server host.
* **Query:** `host.keyword: mailsv`
* **Finding:** Discovered `/mailsv/secure.log` as the primary source for authentication and authorization data.

### 3. Identifying Brute-Force Attempts
I performed a targeted search to locate failed attempts to access the highest-privilege account (root) on the mail server.
* **Query:** `host.keyword: mailsv AND (fail* OR failed) AND root`
* **Results:** Identified **376 events** matching this criteria.



## Key Takeaway
Using a SIEM like Wazuh transforms "noise" into "intelligence." By querying 100,000+ logs in seconds, I was able to pinpoint a specific security risk—376 failed root logins—which strongly suggests an ongoing brute-force attack. This allows for immediate remediation, such as blocking the offending IPs or disabling root SSH access, before a breach occurs.

---
### 📑 Artifacts
* **Platform:** Wazuh Virtual Machine (Open-source SIEM).
* **Data Set:** Buttercup Games tutorial data (Authentication, Email, and Web logs).
* **Key Finding:** 376 Failed SSH root logins on `mailsv`.
