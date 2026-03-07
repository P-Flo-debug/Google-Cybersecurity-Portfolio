# Project 5: File Integrity Analysis via Hashing 🧬

## Project Overview
As a security analyst, ensuring data integrity is critical. This project demonstrates how to use cryptographic hash functions to uniquely identify file contents and verify whether a file has been modified, even if the changes are invisible to the naked eye (e.g., a single malicious line of code in a program).



## Technical Skills & Tools
* **Linux Terminal:** Navigating the Bash shell and managing hidden data.
* **SHA-256 (Secure Hash Algorithm):** Generating unique 256-bit "fingerprints" for data.
* **Integrity Verification:** Manually comparing digests to detect unauthorized changes.
* **Linux Commands:** `sha256sum`, `cmp`, `cat`, and I/O redirection (`>`).

## Step-by-Step Execution

### 1. Visual Inspection vs. Technical Audit
I started with two files, `file1.txt` and `file2.txt`. When using the `cat` command, the text inside both files appeared exactly identical. However, visual inspection is insufficient for security validation.

### 2. Generating SHA-256 Hashes
To find the "digital fingerprint" of each file, I ran:
* `sha256sum file1.txt`
* `sha256sum file2.txt`

**Observation:** The resulting hash values were completely different. This confirmed that despite looking the same, the files were not identical at the byte level.

### 3. Systematic Comparison
I redirected the hash outputs into separate files (`file1hash` and `file2hash`) and used the `cmp` command to perform a byte-by-byte comparison.
* **Command:** `cmp file1hash file2hash`
* **Result:** The system reported a difference at the very first character, confirming a breach of integrity or a variation in the file source.

## Key Takeaway
This lab highlights the **Integrity** component of the CIA Triad. Hashing is a non-negotiable tool for:
1. **Malware Detection:** Identifying if a legitimate software installer has been replaced by a malicious version.
2. **Forensics:** Ensuring evidence has not been altered during an investigation.
3. **Software Updates:** Verifying that a downloaded patch is exactly what the vendor intended to send.

---
### 📑 Artifacts
* [Lab Documentation: Hashing Workflow](./hashing_analysis.md)
