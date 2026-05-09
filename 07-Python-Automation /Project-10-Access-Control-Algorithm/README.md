# Project 10: Automating Access Control Lists

## Project Overview
In this final project for the Python course, I developed a complete algorithm to automate the updating of network access control lists. The script is designed to open a text file containing approved IP addresses, compare it against a list of IP addresses flagged for removal, dynamically update the data, and overwrite the original file with the newly secured list. 

## 🔗 Project Link
* **[View Full Jupyter Notebook](./Activity_Create_another_algorithm.ipynb)**

## Tasks Completed
* **Data Parsing:** Opened a text file (`allow_list.txt`) and used the `.split()` method to convert the raw string data into a workable Python list.
* **Iterative Evaluation:** Built a `for` loop to iterate through the current access list, incorporating an `if` statement to check each IP against a `remove_list`.
* **Dynamic Removal:** Utilized the `.remove()` method to delete unauthorized IP addresses from the active memory list.
* **Format Conversion:** Applied the `.join()` method to convert the updated list back into a single string, formatted with spaces, to prepare it for text file export.
* **File Overwriting:** Reopened the original file using the `"w"` (write) parameter to overwrite the old data with the newly secured access list.
* **Algorithm Encapsulation:** Wrapped the entire process into a single, reusable `update_file(import_file, remove_list)` function for clean, modular code.

## Key Takeaways
> "Key takeaways from this lab include understanding how Python can be used to import, read, and process text files. The with statement is helpful for handling files efficiently because it automatically manages opening and closing them. This lab also demonstrated how for loops can iterate through lists and how if statements can check whether a value exists in a list before carrying out an action. Finally, algorithms can be organized into functions, which improves code structure and reusability."

## Technical Skills Used
* **Language:** Python 3
* **File Operations:** `with open()`, `.read()`, `.write()`
* **Data Type Manipulation:** `.split()`, `" ".join()`
* **Control Flow:** Iteration (`for`), Conditionals (`if/in`)
* **Code Architecture:** User-Defined Functions (`def`)
