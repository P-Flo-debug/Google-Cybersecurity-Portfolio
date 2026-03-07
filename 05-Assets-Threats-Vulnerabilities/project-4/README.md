# Project 4: Decrypt an Encrypted Message 💻

## Scenario
Acting as a security analyst, I navigated a Linux environment to recover critical data files encrypted by a threat actor.

## Technical Execution
1. **Discovery:** Used `ls -a` to find a hidden instruction file (`.leftShift3`).
2. **Cryptanalysis:** Identified a Caesar cipher. Used the `tr` command to "rotate" the alphabet and reveal the passphrase.
   * **Command:** `cat .leftShift3 | tr "d-za-cd-ZA-C" "a-zA-Z"`
3. **Decryption:** Utilized **OpenSSL** with the **AES-256-CBC** algorithm to recover the final data.
   * **Command:** `openssl aes-256-cbc -pbkdf2 -a -d -in Q1.encrypted -out Q1.recovered -k [PASSPHRASE]`

## Key Takeaways
This lab demonstrates the difference between **Obfuscation** (Caesar) and **Strong Encryption** (AES), and the importance of command-line proficiency in incident response.

### 📑 Artifacts
* [Terminal Lab Screenshot](./Decryption_Lab.png)
