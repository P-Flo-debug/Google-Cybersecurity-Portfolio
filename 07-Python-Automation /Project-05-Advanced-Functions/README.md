# Project 5: Advanced Functions and Log Analysis

## Project Overview
In this project, I expanded my knowledge of Python functions by combining built-in list operations with custom-defined logic. The primary objective was to analyze failed login attempts, identify outliers, and build a reusable tool that evaluates whether a specific user's login activity requires further investigation based on historical averages.

## 🔗 Project Link
* **[View Full Jupyter Notebook](./Activity_Create_more_functions.ipynb)**

## Tasks Completed
* **Data Sorting:** Utilized the built-in `sorted()` function to organize a list of monthly failed login attempts in ascending numerical order, making it easier to spot trends.
* **Outlier Identification:** Applied the `max()` function to isolate the highest number of failed logins from a dataset, pinpointing the exact month requiring investigation.
* **Custom Function Parameters:** Defined the `analyze_logins()` function to accept multiple arguments (`username`, `current_day_logins`, and `average_day_logins`).
* **Data Handling via Returns:** Calculated the ratio of current logins to average logins and used the `return` statement to pass that data out of the function for further use.
* **Threshold Alerting:** Implemented a conditional `if` statement outside the function to evaluate the returned ratio, triggering a security alert if the login activity was 3 or more times higher than normal.

## Key Takeaways
> "Python functions are flexible tools that can be designed to either display information directly to the screen or return data to be captured in a variable for later use. By accepting various parameters, these functions can execute complex sequences of tasks to produce a specific result. For instance, built-in tools like sorted() and max() process lists to return organized data or identify the highest value, respectively."

## Technical Skills Used
* **Language:** Python 3
* **Built-in Functions:** `sorted()`, `max()`, `print()`
* **User-Defined Functions:** Multiple parameters, `def`, `return` keyword
* **Logic:** Conditional thresholds (`>=`), Variable assignment from function outputs
