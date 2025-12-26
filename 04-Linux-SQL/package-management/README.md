# Linux Package Management: Suricata & tcpdump

## 🛡️ Project Overview
In this project, I demonstrated the ability to manage software on a Linux-based security workstation using the **Advanced Package Tool (APT)**. As a security professional, controlling which applications are installed on a system is critical for maintaining a low attack surface and ensuring that essential monitoring tools are available for incident response.

## 🛠️ Tools & Environments
* **Operating System:** Linux (Bash Shell)
* **Package Manager:** APT (Advanced Package Tool)
* **Security Tools:** * **Suricata:** An open-source Intrusion Detection System (IDS).
    * **tcpdump:** A command-line packet analyzer for network traffic.

## 🚀 Lab Tasks & Execution

### 1. Environment Verification
Before installing tools, I verified the presence of the package manager:
`apt --version`

### 2. Installing Security Monitoring Tools
I used superuser privileges (`sudo`) to install Suricata:
`sudo apt install suricata`

### 3. Software Lifecycle & Surface Area Reduction
I demonstrated the removal of software to reduce the potential attack surface:
`sudo apt remove suricata`
`sudo apt install tcpdump`

### 4. Reinstallation & Verification
Finally, I reinstalled Suricata to confirm the package index was up to date:
`sudo apt install suricata`

---

## 🧠 Key Security Concepts Learned
* **The Principle of Least Functionality:** Only installing necessary tools to minimize security risks.
* **Administrative Control:** Using `sudo` to manage system-level changes securely.
* **Dependency Management:** Understanding how APT handles the installation of libraries required by security tools.
