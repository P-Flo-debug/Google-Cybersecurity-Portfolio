# Apply filters to SQL queries

## Project description
In this activity, I applied SQL filtering techniques to an organizational database to retrieve specific security-related data. The objective was to investigate potential security issues, such as failed login attempts, and to organize data needed for system updates. I used various SQL operators to refine queries, including AND, OR, NOT, and LIKE, as well as filtering by specific dates and times.

## Retrieve after hours failed login attempts
To investigate potential unauthorized access, I filtered the `log_in_attempts` table for unsuccessful attempts (represented by a Boolean `0` or `FALSE`) that occurred after 18:00. I used the `AND` operator to ensure both conditions were met simultaneously.

* **Query:** `SELECT * FROM log_in_attempts WHERE login_time > '18:00' AND success = 0;`
* **Explanation:** This query selects all columns where the time is after 18:00 **AND** the success column is 0, indicating an unsuccessful login attempt.

## Retrieve login attempts on specific dates
I searched for activity occurring during a specific incident window on May 8th and May 9th, 2022. This required the `OR` operator to capture records from either date.

* **Query:** `SELECT * FROM log_in_attempts WHERE login_date = '2022-05-08' OR login_date = '2022-05-09';`
* **Explanation:** By using `OR`, the query retrieves rows if the `login_date` matches either of the two specified values.

## Retrieve login attempts outside of Mexico
To identify international login activity, I used the `NOT` operator combined with `LIKE` and a wildcard. This excluded all entries starting with the pattern 'MEX'.

* **Query:** `SELECT * FROM log_in_attempts WHERE NOT country LIKE 'MEX%';`
* **Explanation:** The `NOT` operator reverses the logic, while `LIKE 'MEX%'` uses the `%` wildcard to catch variations like "MEX" or "MEXICO".



## Retrieve employees in Marketing
I identified employees in the Marketing department who work in the East building. This required pattern matching for the office location.

* **Query:** `SELECT * FROM employees WHERE department = 'Marketing' AND office LIKE 'East%';`
* **Explanation:** The `AND` operator ensures the employee is in Marketing, and `LIKE 'East%'` filters for any office number within the East building.

## Retrieve employees in Finance or Sales
I retrieved records for two departments simultaneously to facilitate specialized security updates.

* **Query:** `SELECT * FROM employees WHERE department = 'Finance' OR department = 'Sales';`
* **Explanation:** Using `OR` allows the results to include employees who belong to either the Finance department or the Sales department.

## Retrieve all employees not in IT
To identify employees who still needed an update that had already been deployed to the IT department, I used an exclusion filter.

* **Query:** `SELECT * FROM employees WHERE NOT department = 'Information Technology';`
* **Explanation:** The `NOT` operator excludes any record where the department is 'Information Technology', returning all other staff members.

## Summary
In this lab, I practiced advanced data retrieval using SQL filters. I successfully used `AND` and `OR` to handle multiple conditions and `NOT` to exclude irrelevant data. I also applied `LIKE` with wildcards (`%`) for pattern matching and filtered by specific dates and times. These skills are fundamental for security analysts to efficiently extract actionable insights from large datasets.

---

## 📝 Personal Insights
During this lab, I learned that combining logical operators allows for much more precise investigations. The `LIKE` operator is especially useful when dealing with naming conventions, such as building names or country codes, that might have slight variations. I also recognized how important it is to distinguish between Boolean data (like success/failure) and string data when writing queries to avoid errors.
