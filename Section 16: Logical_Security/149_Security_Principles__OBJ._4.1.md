## 💡 Security Principles (OBJ 4.1)

This section covers fundamental security principles that are crucial for protecting networks and data.

✅ **1. Principle of Least Privilege**
- **Definition:** Users (or systems/devices) should operate with the lowest level of permissions or privileges needed to complete their job function or task.
- **Application:**
  - **User Accounts:** Use a regular user account for daily tasks; log in as administrator only when necessary.
  - **System Design:** IoT devices should only have access to the specific ports/services they need. Isolate them in separate VLANs/subnets.

✅ **2. Access Control Models**
- **Purpose:** Methods for conducting access control in a network.
- **a. Discretionary Access Control (DAC):**
  - **Definition:** Access is determined by the owner of that resource. The owner assigns permission levels (read, write, run) to other users.
  - **Pros:** Very granular control. Owner is most knowledgeable about their resource.
  - **Cons:** Every object needs an owner. Relies on owners to set permissions correctly (can be too tight, too loose, or not set at all). Can be dangerous in corporate environments if not managed well.
- **b. Mandatory Access Control (MAC):**
  - **Definition:** Access control policy where the computer system (not the owner) decides who has access to what objects, based on data labels.
  - **Mechanism:** Subjects (users) and objects (data) are assigned trust levels/clearance labels (e.g., Unclassified, Confidential, Secret, Top Secret). Access is granted if the subject's clearance level is at or above the object's classification level, AND the subject has a "need to know."
  - **Pros:** Very high security.
  - **Cons:** Very complex to implement and manage.
  - **Use:** Primarily in high-security environments like the military.
- **c. Role-Based Access Control (RBAC):**
  - **Definition:** Access model controlled by the system (like MAC), but focuses on sets of permissions assigned to roles, rather than individual users or data labels.
  - **Mechanism:** Create roles for job functions (e.g., Sales, HR, IT Admin, Power User). Assign permissions to these roles. Assign users to roles.
  - **Pros:** Best practice in cybersecurity. Easier to manage permissions at scale (add/remove users from roles instead of individual files). Enforces least privilege by relating permissions to job functions.
  - **Example:** A "Power User" role in Windows has more permissions than a regular user (e.g., add printer, change time) but less than a full administrator.