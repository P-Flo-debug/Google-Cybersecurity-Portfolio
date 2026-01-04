# SQL Logic: Applying Complex Filters (AND, OR, NOT)

## 🛡️ Project Overview
In this project, I demonstrated the ability to use Boolean logic in SQL to perform advanced security investigations. As a security analyst, I practiced combining multiple conditions to narrow down results and using exclusion logic to remove irrelevant data. These skills are essential for identifying suspicious activity that meets several high-risk criteria simultaneously.

## 🛠️ SQL Operators & Skills Applied
* **AND:** Combined multiple criteria that must all be true (e.g., failed logins + after-hours).
* **OR:** Retrieved records matching at least one of several conditions (e.g., multiple departments or dates).
* **NOT:** Excluded specific data points to focus on outliers (e.g., all countries except Mexico).
* **Boolean Logic:** Applied 1 (TRUE) and 0 (FALSE) values for success/failure auditing.
* **Pattern Matching:** Combined logic with the `LIKE` operator for flexible filtering.

## 🚀 Lab Walkthrough

### 1. Identifying High-Risk Login Failures
I investigated unsuccessful login attempts occurring after standard business hours (18:00). By using `AND`, I isolated 19 specific events where both the time was late and the `success` value was 0 (FALSE).
* **Query:** `SELECT * FROM log_in_attempts WHERE login_time > '18:00' AND success = 0;`

### 2. Investigating Specific Incident Windows
To analyze a suspicious event period, I used `OR` to pull all login attempts from two consecutive days (May 8th and 9th, 2022). This allowed for a comprehensive view of activity across the entire incident window.
* **Query:** `SELECT * FROM log_in_attempts WHERE login_date = '2022-05-08' OR login_date = '2022-05-09';`

### 3. Geographical Exclusion Audits
I filtered for logins originating outside of Mexico to identify potential foreign unauthorized access. Using `NOT` with `LIKE 'MEX%'` allowed me to exclude all variations of the country name.
* **Query:** `SELECT * FROM log_in_attempts WHERE NOT country LIKE 'MEX%';`

### 4. Role-Based Data Retrieval
I performed several organizational audits using logical operators:
* **Departmental Pattern Matching:** Found employees in 'Marketing' specifically located in the 'East' building using `AND` and `LIKE 'East%'`.
* **Multi-Department Filtering:** Used `OR` to locate all staff in either 'Finance' or 'Sales' for specialized security updates.
* **Exclusion Filtering:** Used `NOT` to identify all employees outside of the 'Information Technology' department to track update progress.

---

## 🧠 Security Perspective
Why is Boolean logic critical for a Security Professional?
1. **Correlation:** Attackers often hide in the "middle" of logs. `AND` allows an analyst to correlate different behaviors (like a specific user + a specific IP + a specific time) to confirm a threat.
2. **Noise Reduction:** `NOT` is one of the most powerful tools for threat hunting. By filtering out "known good" activity (like IT department logins or domestic traffic), analysts can see the suspicious outliers that remain.
3. **Inclusive Searching:** During an active breach, an analyst might need to watch multiple departments or server IDs at once. `OR` ensures no critical data is missed.

---

## 📝 Personal Insights
Learning to combine `AND` and `OR` felt like learning to build a digital filter. I realized that the order of these commands is very important for the results. It was also interesting to see that SQL uses `1` and `0` for TRUE and FALSE—this reminds me of the binary basics I learned earlier in the course.
