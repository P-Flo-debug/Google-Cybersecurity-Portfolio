# SQL Joins: Connecting Security Data Across Tables

## Project description
In this activity, I used SQL joins to combine data from multiple tables within an organizational database to investigate a security incident. As a security analyst, retrieving information across tables is essential when data like employee details, machine specifications, and login logs are stored separately. I practiced using `INNER JOIN`, `LEFT JOIN`, and `RIGHT JOIN` to identify relationships between users and assets and to audit gaps in machine assignments.

## Match employees to their machines
I performed an inner join to identify which employees are currently assigned to which machines. By linking the `employees` and `machines` tables on their common `device_id` column, I was able to see the specific pairing of hardware to users.
* **Query:** `SELECT * FROM machines INNER JOIN employees ON machines.device_id = employees.device_id;`
* **Explanation:** This query returns only the records where there is a match in the `device_id` column in both tables. This resulted in 185 rows of matched data.

## Return more data with Left and Right Joins
I used outer joins to identify discrepancies in the inventory, such as machines without assigned users or employees without assigned machines.
* **Left Join Query:** `SELECT * FROM machines LEFT JOIN employees ON machines.device_id = employees.device_id;`
* **Explanation:** This query includes all records from the `machines` table (the "left" table). Where a machine had no assigned employee, the username appeared as `NULL`.
* **Right Join Query:** `SELECT * FROM machines RIGHT JOIN employees ON machines.device_id = employees.device_id;`
* **Explanation:** This query includes all records from the `employees` table (the "right" table). This allowed me to identify all employees, regardless of whether they had a machine assigned to them in the database.



## Retrieve login attempt data
To assist in the incident investigation, I needed to correlate employee identities with specific login attempts. I performed an inner join between the `employees` and `log_in_attempts` tables using the common `username` column.
* **Query:** `SELECT * FROM employees INNER JOIN log_in_attempts ON employees.username = log_in_attempts.username;`
* **Explanation:** This query combined employee background information with their specific login activity. I used the `table.column` syntax to clearly define the relationship between the two tables. This join returned 200 records.

## Summary
In this lab, I gained practical experience using different types of SQL joins to merge datasets. I used `INNER JOIN` to find direct matches between employees and devices, and used `LEFT` and `RIGHT` joins to identify unassigned assets or users. These techniques are vital for security analysts when building a complete picture of an environment during an investigation.

---

## 📝 Personal Insights
This lab made me realize how relational databases are structured to stay organized. At first, the difference between a Left Join and a Right Join was confusing, but seeing the `NULL` values helped me understand that "Left" and "Right" just refer to which table's data you want to keep entirely. I also learned that using `table.column` notation is a best practice to keep queries clear and prevent the database from getting confused when two tables share the same column names.
