# Project 6: String Manipulation for Security Data

## Project Overview
In this project, I practiced working with string data, which is essential for handling security information like device IDs, URLs, and employee records. The focus was on automating the extraction of specific data points and standardizing text formats using Python's built-in string methods.

## 🔗 Project Link
* **[View Full Jupyter Notebook](./Activity_Work_with_strings_in_Python.ipynb)**

## Tasks Completed
* **Data Type Conversion:** Used the `str()` function to convert integer-based employee IDs into strings for text manipulation.
* **Format Standardization:** Implemented the `len()` function and conditional logic to identify non-compliant employee IDs, using string concatenation (`+`) to add missing prefix characters.
* **Data Extraction (Slicing):** Used bracket notation to slice specific characters from alphanumeric device IDs (e.g., `device_id[0:3]`).
* **Dynamic URL Parsing:** Applied the `.index()` method to locate the exact starting position of domain extensions (like ".com") to dynamically slice and extract website names and protocols from URLs.

## Key Takeaways
> "Strings play a vital role in storing critical security data, such as device IDs and URLs, and Python offers a variety of powerful tools to manipulate them. You can seamlessly combine information using string concatenation or extract specific subsections through string slicing. To further assist analysts in working with these values, Python includes several built-in functions: type(), str(), len(), and the .index() method."

## Technical Skills Used
* **Language:** Python 3
* **String Methods:** `.index()`
* **Built-in Functions:** `type()`, `str()`, `len()`
* **Concepts:** String Slicing (`[x:y]`), String Concatenation, Dynamic Indexing
