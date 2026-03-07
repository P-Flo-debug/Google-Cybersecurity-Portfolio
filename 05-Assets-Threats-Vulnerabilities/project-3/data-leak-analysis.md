# Data Leak Analysis Worksheet

## Incident Overview
**Scenario:** A manager shared a folder containing both public marketing materials and sensitive internal analytics with a representative but failed to revoke access. The representative accidentally shared the entire folder link with an external partner, leading to a public data leak on social media.

---

## Analysis Tasks

### 1. Issue Identification
The data leak was primarily caused by a failure to revoke access permissions after a specific business need was met, combined with human error during information sharing. The manager’s oversight in leaving the folder accessible allowed a representative to accidentally share internal-only analytics rather than just the intended promotional materials.

### 2. NIST SP 800-53: AC-6 Review
NIST SP 800-53: AC-6 defines the principle of **least privilege**, which mandates that users should only be granted the minimum level of access necessary to perform their specific job functions. This framework is designed to be customizable, helping businesses prevent users from operating at privilege levels higher than required for their objectives.



### 3. Control Enhancement Recommendations
Based on the NIST SP 800-53: AC-6 control enhancements, the following improvements should be implemented:
* **Role-Based Access Control (RBAC):** Restrict access based on user role to ensure sales representatives only have access to "External" folders, while "Internal" analytics remain restricted to management.
* **Automated Access Expiration:** Implement a policy where access to sensitive internal folders expires automatically after a set period, such as the conclusion of a meeting, to remove reliance on manual revocation.

### 4. Professional Justification
Implementing these enhancements will reduce the likelihood of future leaks by removing the "human error" factor of forgetting to unshare files. By automating access expiration and enforcing role-based restrictions, the company ensures that even if a link is shared accidentally, unauthorized external parties will be blocked by the system's underlying permission structure.
