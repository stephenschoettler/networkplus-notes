## 💡 Identity and Access Management (IAM) (OBJ 4.1)

Identity and Access Management (IAM) is a security process that provides identification, authentication, and authorization mechanisms for users, computers, and other entities to work with organizational assets (networks, OS, applications).

✅ **Core Components**
- **Identification:** Unique subject in the organization is identified and associated with an account.
- **Authentication:** Proving identity (e.g., username/password).
- **Authorization:** Granting permissions to access certain things.

✅ **Unique Subjects in IAM**
- **1. Personnel:** Human users (employees).
- **2. Endpoints:** Desktops, laptops, tablets, cell phones – devices users log onto.
- **3. Servers:** Backend machines, often for machine-to-machine communication.
- **4. Software:** Applications that interact with users/systems.
- **5. Roles:** Define resources an asset has permission to access based on its function. Can be assigned to people, servers, endpoints, or software.

✅ **IAM Tasks**
- **Technical Components:** Directory services, access management tools, auditing/reporting systems.
- **Account Management:** Provisioning, deprovisioning, managing (passwords, certificates, permissions), auditing.
- **Evaluating Identity-Based Threats:** Running password checks for weak passwords.
- **Maintaining Compliance:** Ensuring the system meets security requirements through audits and checks.

✅ **Risks within IAM (Account Types)**
- **1. User Accounts:** Standard accounts with basic permissions. Least risky.
- **2. Privileged Accounts:** (Administrator, root, superuser). Have extensive permissions. Highly risky. Require additional auditing and compliance checks.
- **3. Shared Accounts:** (e.g., one account for multiple users in SOHO). Very dangerous. Lose ability to audit who performed actions. Not recommended.
- **Recommendation:** Use individual user accounts and role-based permissions.