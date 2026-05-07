# Project 8: Parsing Security Logs with Regular Expressions

## Project Overview
In this project, I utilized Python's `re` module to automate the parsing of raw security logs. As a security analyst, log files are often unstructured and massive. By writing custom Regular Expressions (Regex), I developed scripts to instantly extract targeted data points, such as devices requiring critical updates and valid IP addresses, while ignoring formatting errors and invalid entries.

## 🔗 Project Link
* **[View Full Jupyter Notebook](./Activity_Use_regular_expressions_to_find_patterns.ipynb)**

## Tasks Completed
* **Module Implementation:** Imported and utilized the `re` module, specifically the `re.findall()` function, to scan string data for specific patterns.
* **Alphanumeric Extraction:** Created a regex pattern (`r15\w+`) to identify specific device IDs running an outdated operating system requiring a security patch.
* **Pattern Refinement:** Developed a highly specific regex pattern (`\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}`) to extract correctly formatted IPv4 addresses while filtering out invalid log entries (e.g., segments with more than three digits).
* **Automated Threat Detection:** Combined regex extraction with an iterative `for` loop to cross-reference the extracted IP addresses against a list of known flagged addresses, generating automated alerts for further investigation.

## Key Takeaways
> "Regular expressions in Python are used to define patterns that help locate and extract important strings from text. Several regex symbols were used in this lab. For example, \w matches any alphanumeric character, + indicates one or more occurrences, \d matches any digit, and \. represents a literal period. Additionally, {x,y} is used to specify a range."

## Technical Skills Used
* **Language:** Python 3
* **Libraries:** `re`
* **Regex Patterns:** `\w`, `\d`, `\.`, `+`, `{x,y}`
* **Functions:** `re.findall()`
* **Logic:** Iterating through regex match lists and cross-referencing with flagged data arrays.
