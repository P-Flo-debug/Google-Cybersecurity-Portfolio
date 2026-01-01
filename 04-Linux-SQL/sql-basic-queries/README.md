# SQL Basics: Retrieving and Sorting Security Data

## 🛡️ Project Overview
As a security analyst, I often need to extract specific data from large databases to investigate potential threats or audit system compliance. In this project, I used SQL (Structured Query Language) to query an organization's database. I focused on retrieving device information for system updates and investigating login logs for unusual patterns, ensuring the data was organized and actionable.

## 🛠️ SQL Syntax & Skills
* **SELECT:** Specified the exact data columns needed for investigation.
* **FROM:** Identified the source tables (`machines` and `login_attempts`).
* **The Asterisk (*):** Used as a wildcard to retrieve all data fields from a table.
* **ORDER BY:** Sequenced results by date and time to create a chronological timeline of events.

## 🚀 Lab Walkthrough

### 1. Auditing System Inventory
I queried the `machines` table to identify which devices required operating system patches. By selecting specific columns like `device_id`, `operating_system`, and `OS_patch_date`, I created a targeted list for the IT team.
* **Key Query:** `SELECT device_id, operating_system, OS_patch_date FROM machines;`

### 2. Investigating Login Logs
I analyzed the `login_attempts` table to monitor for unauthorized access. I specifically looked for login attempts originating from unexpected countries or occurring outside of standard business hours.
* **Key Query:** `SELECT username, login_date, login_time FROM login_attempts;`

### 3. Chronological Event Analysis
To better understand the timing of login events, I used the `ORDER BY` keyword. Sorting the logs by `login_date` and `login_time` allowed me to see the exact sequence of user activity, which is vital during a forensic investigation.
* **Key Query:** `SELECT * FROM login_attempts ORDER BY login_date, login_time;`

---

## 🧠 Security Perspective
Why do these SQL basics matter to a Security Professional?
1. **Visibility:** You cannot protect what you cannot see. SQL provides the visibility needed to track every device and every login attempt in an organization.
2. **Efficiency:** Using `SELECT` for specific columns instead of `SELECT *` reduces system load and allows analysts to focus only on relevant "Indicators of Compromise" (IoCs).
3. **Incident Timeline:** The `ORDER BY` clause is essential for reconstructing a security incident. Knowing the *order* in which an attacker moved through a system is just as important as knowing *what* they accessed.

---

## 📝 My Personal Insights
I realized that SQL is very similar to the Linux commands I just learned—it's all about filtering out the noise to find the important data. I found the `ORDER BY` command really helpful because it makes messy logs look organized instantly.
