# SQL Filtering: Investigative Data Retrieval

## 🛡️ Project Overview
In this project, I practiced using SQL filters to retrieve specific security-related data from an organization's database. As a security analyst, being able to narrow down thousands of records to find a specific building, department, or operating system is a core skill for incident response and system auditing. I used the `WHERE` clause and the `LIKE` operator to perform targeted searches on employee and machine data.

## 🛠️ SQL Skills Applied
* **WHERE Clause:** Filtered query results to show only records meeting specific criteria (e.g., specific operating systems).
* **LIKE Operator:** Performed pattern matching to find groups of data based on partial strings.
* **Wildcards (%):** Used the percent sign to capture all entries related to a specific building location.
* **Data Auditing:** Practiced isolating departments (Finance and Sales) to ensure security notices were sent to the correct personnel.

## 🚀 Lab Walkthrough

### 1. Identifying Vulnerable Systems
I was tasked with finding all machines running "OS 2" to prepare for a critical update. Using the `WHERE` clause, I filtered 200 total records down to the specific 80 devices requiring attention.
* **Query:** `SELECT * FROM machines WHERE operating_system = 'OS 2';`

### 2. Targeted Department Audits
To assist with a privacy notice distribution, I filtered the `employees` table to identify staff in the 'Finance' and 'Sales' departments. This demonstrated how to pull office numbers for specific organizational units.
* **Query:** `SELECT * FROM employees WHERE department = 'Finance';`

### 3. Pattern Matching for Physical Security
My team identified an issue affecting all machines in the 'South' building. Using the `LIKE` operator with a wildcard, I was able to pull every employee record associated with that building, regardless of the specific office number.
* **Query:** `SELECT * FROM employees WHERE office LIKE 'South%';`

---

## 🧠 Security Perspective
Why is filtering critical for a Security Professional?
1. **Precision:** In an incident, speed is vital. Filtering allows an analyst to ignore "noise" and find the exact user or machine involved in a breach.
2. **Compliance:** Auditing specific departments (like Finance) ensures that users handling sensitive data are following the correct security protocols.
3. **Forensics:** Using pattern matching (`LIKE`) helps analysts find related events, such as multiple login failures from the same subnet or building.

---

## 📝 Personal Insights
This lab showed me how powerful a single line of SQL can be. It was interesting to see how the `WHERE` clause can instantly turn a huge table into a small, manageable list. I also realized that the `LIKE` operator is a lot like the `grep` command I learned in Linux—it’s all about finding patterns to get to the truth faster.
