# Project 9: File Handling and Log Parsing

## Project Overview
In this project, I demonstrated how to use Python to manage and analyze text-based security logs. Since security information is often stored in text files, I practiced automating the workflow of importing logs, parsing large blocks of text into manageable data structures, updating records, and exporting new security lists.

## 🔗 Project Link
* **[View Full Jupyter Notebook](./Activity_Import_and_parse_a_text_file.ipynb)**

## Tasks Completed
* **Importing and Reading:** Used the `with open()` statement and the `"r"` (read) parameter to securely open and read security logs into a string variable.
* **Data Parsing:** Applied the `.split()` method to convert a massive, continuous string of log data into a clean, iterable list, separated line-by-line.
* **Appending Data:** Used the `"a"` (append) parameter to dynamically add missing log entries to the end of an existing log file without overwriting historical data.
* **Exporting Security Lists:** Created a brand new text file (`allow_list.txt`) using the `"w"` (write) parameter to export a compiled list of approved IP addresses for team distribution.

## Key Takeaways
> "Key takeaways from this lab include learning how Python can be used to import, read, and modify text files. The with statement is useful because it manages files efficiently and automatically handles closing them after use. The open() function is used to access a file, with the first argument specifying the filename and the second argument determining the file mode."

## Technical Skills Used
* **Language:** Python 3
* **File Operations:** `with open()`, `.read()`, `.write()`
* **File Modes:** Read (`"r"`), Write (`"w"`), Append (`"a"`)
* **String Parsing:** `.split()`
