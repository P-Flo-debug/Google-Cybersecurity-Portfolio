# SQL Advanced Filtering: Precise Data Retrieval

## 🛡️ Project Overview
In this project, I used advanced SQL filtering techniques to investigate specific security events within an organization's login logs. As part of a security analysis team, I demonstrated how to use comparison operators and date ranges to isolate suspicious activity, analyze specific timeframes, and retrieve individual records using unique identifiers.

## 🛠️ SQL Operators & Skills Applied
* **Comparison Operators:** Used `>`, `>=`, `<`, `<=`, and `=` to filter data based on numerical and chronological values.
* **BETWEEN:** Applied this operator to retrieve records within a specific, inclusive range of dates.
* **Temporal Filtering:** Practiced querying specific `login_date` and `login_time` formats to pinpoint events.
* **ID-Based Retrieval:** Used unique `login_id` values to extract specific event details.

## 🚀 Lab Walkthrough

### 1. Investigating Recent Activity
I filtered the `log_in_attempts` table to find all logins occurring after a specific threshold (January 15, 2023). This is a common task when an analyst needs to review activity following a known system change or alert.
* **Query:** `SELECT * FROM log_in_attempts WHERE login_date > '2023-01-15';`

### 2. Analyzing Date Ranges
To review activity during a specific week in February, I used the `BETWEEN` operator. This allowed for an inclusive search of all attempts from February 1st through February 7th.
* **Query:** `SELECT * FROM log_in_attempts WHERE login_date BETWEEN '2023-02-01' AND '2023-02-07';`

### 3. Pinpointing Specific Timestamps
I conducted a targeted search for login attempts occurring at an exact time (09:30:00) to investigate a reported system anomaly.
* **Query:** `SELECT * FROM log_in_attempts WHERE login_time = '09:30:00';`

### 4. Direct Record Access
Using the `login_id`, I retrieved a single, specific record (ID 503). In a real-world scenario, this allows an analyst to quickly pull all metadata associated with a suspicious event ID flagged by an automated system.
* **Query:** `SELECT * FROM log_in_attempts WHERE login_id = 503;`

---

## 🧠 Security Perspective
Why is precise filtering critical for a Security Professional?
1. **Forensic Timelines:** Security incidents are often reconstructed by looking at what happened between two specific points in time. Operators like `BETWEEN` and `>` are essential for building these timelines.
2. **Alert Investigation:** When a Security Information and Event Management (SIEM) tool flags a specific `login_id`, the analyst must be able to use SQL to pull that exact record for review.
3. **Data Volume Management:** Databases can contain millions of rows. Precise filtering prevents "information overload" and allows an analyst to focus on the small subset of data that actually matters for the investigation.

---

## 📝 Personal Insights
This lab taught me that SQL isn't just for broad searches; it's a precision tool. I found it very useful to see how specific time formats (HH:MM:SS) are handled. It reminded me of the "Time-of-Check to Time-of-Use" concepts in security—being able to prove exactly when a user accessed a system is vital for accountability.
