# Project 10: Threat Modeling with the PASTA Framework 🍝🛡️

## Project Overview
In this project, I performed a comprehensive threat model for a mobile sneaker marketplace using the **PASTA (Process for Attack Simulation and Threat Analysis)** framework. Unlike simple vulnerability scans, PASTA allowed me to simulate attacker behavior and map technical weaknesses (like SQL injection) to business impacts (like loss of customer trust and PCI-DSS non-compliance).

## Technical Skills & Tools
* **Threat Modeling Frameworks:** PASTA (Stages I-VII).
* **Application Security:** Decomposing APIs, SQL databases, and PKI.
* **Diagramming:** Creating Data Flow Diagrams (DFD) and Attack Trees.
* **Risk Mitigation:** Aligning technical controls (SHA-256, Prepared Statements) with business goals.



## The PASTA Process

### 1. Decomposing the Application (Stage III)
I analyzed how data moves from the user to the database. I identified the **Application Programming Interface (API)** as the highest priority for security testing, as it serves as the bridge between the mobile app and sensitive backend services.



### 2. Threat & Vulnerability Analysis (Stages IV & V)
I identified two critical technical risks based on the app's architecture:
* **SQL Injection:** Due to a potential lack of prepared statements in the search function.
* **Session Hijacking:** Vulnerabilities in how cookies are handled between the app and the server.

### 3. Attack Modeling (Stage VI)
I developed an **Attack Tree** to visualize the paths an intruder could take to compromise user data. This helped validate that the technical vulnerabilities identified were viable paths for a threat actor.



### 4. Risk Analysis & Impact (Stage VII)
To protect the marketplace before launch, I recommended a multi-layered defense strategy:
* **Technical:** Implementing SHA-256 hashing for data integrity and using **Prepared Statements** to neutralize SQL injection.
* **Operational:** Establishing incident response procedures and regular log monitoring.
* **Managerial:** Enforcing a strong password policy and the Principle of Least Privilege (PoLP).

## Key Takeaway
Threat modeling with PASTA ensures that security is baked into the development lifecycle rather than added as an afterthought. It allows an organization to spend its security budget on the threats that actually matter to the business.

---
### 📑 Artifacts
* [Full PASTA Analysis Worksheet](./PASTA-worksheet.pdf)
* [Data Flow Diagram (Visualized)](./PASTA-data-flow-diagram.pdf)
* [Attack Tree Model](./PASTA-attack-tree.pdf)
