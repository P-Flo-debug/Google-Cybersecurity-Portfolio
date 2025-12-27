# Linux File Investigation: Navigation and Discovery

## 🛡️ Project Overview
As a security analyst, the ability to navigate a file system and quickly locate sensitive logs or configuration files is critical for incident response. In this project, I demonstrated how to explore a Linux directory structure and inspect file contents using the Bash shell.

## 🛠️ Commands & Skills
* **pwd:** Print Working Directory—used to confirm current location within the file system.
* **ls:** List Directory Contents—used to audit files and subdirectories.
* **cd:** Change Directory—used to move through the system hierarchy.
* **cat:** Concatenate—used to read the entire contents of a file.
* **head:** Used to display the top 10 lines of a file, essential for a quick look at log headers.

## 🚀 Lab Walkthrough

### 1. Mapping the Environment
I began by identifying the current working directory and listing all available files to establish a baseline for the investigation.
Example: `pwd` and `ls -l`

### 2. Navigating the Hierarchy
I moved through the system to specific directories to locate subdirectories, simulating the search for specific system logs.
Example: `cd /home/analyst/logs`

### 3. Inspecting File Contents
I used the `cat` command to read a full file and the `head` command to inspect only the first 10 lines. In a real-world scenario, `head` is preferred for very large log files to save system resources and time.
Example: `head access_log.txt`

---

## 🧠 Security Perspective
Why do these navigation skills matter to a Security Professional?

1. **Efficiency in Incident Response:** During a live breach, an analyst must know exactly where logs are stored (like `/var/log`) and how to find them without using a GUI.
2. **Resource Management:** Using `head` or `tail` to view the start or end of a file prevents the system from crashing when trying to open massive multi-gigabyte log files.
3. **Audit Readiness:** Being able to quickly list directory contents helps identify "hidden" files or unauthorized scripts left behind by an attacker.
