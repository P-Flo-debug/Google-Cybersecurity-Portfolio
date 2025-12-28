# Linux File System Management: Organization and Editing

## 🛡️ Project Overview
Organization is a key component of effective security analysis. In this project, I acted as a security analyst responsible for auditing and reorganizing the `/home/analyst` directory. This involved creating new directories for logs, removing obsolete files and subdirectories to reduce clutter, and documenting my actions using a command-line text editor.

## 🛠️ Commands & Skills
* **mkdir:** Created new directory structures for log storage.
* **rmdir / rm:** Safely removed obsolete directories and individual files.
* **mv:** Relocated sensitive patch reports to the correct subdirectory.
* **touch:** Created new files for documentation purposes.
* **nano:** Used a command-line text editor to modify and save file content.

## 🚀 Lab Walkthrough

### 1. Directory Restructuring
I created a new `logs` directory to prepare for future data collection and removed a temporary directory (`temp`) that was no longer required for system operations.
* **Commands:** `mkdir logs`, `rmdir temp`

### 2. File Relocation and Cleanup
I moved the `Q3patches.txt` file from the `notes` folder to `reports` to ensure the data was properly categorized. I also deleted `tempnotes.txt` to maintain a clean workspace.
* **Commands:** `mv notes/Q3patches.txt reports/`, `rm notes/tempnotes.txt`

### 3. Documentation with Nano
Using the `touch` command, I created a file called `tasks.txt`. I then used the **nano** text editor to document my administrative actions directly from the terminal.
* **Commands:** `touch notes/tasks.txt`, `nano notes/tasks.txt`

---

## 🧠 Security Perspective
Why does file management matter for security?
1. **Data Integrity:** Keeping reports in specific, organized folders ensures that analysts can find critical data quickly during an incident.
2. **Reducing Attack Surface:** Removing temporary files (`temp`) and old notes reduces the amount of "stale" data that could potentially contain sensitive information or
