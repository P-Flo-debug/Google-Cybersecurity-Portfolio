# Project 7: Developing a Security Access Algorithm

## Project Overview
In this project, I developed a Python algorithm to automate a core Identity and Access Management (IAM) task: verifying whether a user is approved to access a system and ensuring they are using their correctly assigned device. This involved mapping data between synchronized lists and building nested conditional logic to handle various access scenarios.

## 🔗 Project Link
* **[View Full Jupyter Notebook](./Activity_Develop_an_algorithm.ipynb)**

## Tasks Completed
* **List Management:** Maintained organizational security data by using the `.append()` method to onboard new employees and the `.remove()` method to revoke access for departing employees.
* **Synchronized Data Mapping:** Utilized the `.index()` method to link elements across two parallel lists, correlating a specific `username` with their corresponding `device_id`.
* **Access Control Logic:** Built a custom `login()` function utilizing nested `if/elif/else` statements to evaluate access.
* **Automated Alerting:** Designed the algorithm to output specific console messages detailing the exact reason for an access approval or denial (e.g., unrecognized user vs. unrecognized device).

## Key Takeaways
> "Indexing in a list works much like indexing in a string, where positions begin at 0. The .append() method lets you add a new item to the end of a list, while .remove() allows you to delete a specific item. When two lists are organized in the same order and their elements correspond, you can use their indices to match related values between them. Functions are useful for building algorithms."

## Technical Skills Used
* **Language:** Python 3
* **Data Structures:** Lists (Synchronized mapping)
* **List Methods:** `.append()`, `.remove()`, `.index()`
* **Control Flow:** Nested Conditional Statements (`if`, `elif`, `else`)
