## 💡 Network Access Control (NAC) (OBJ 4.3)

Network Access Control (NAC) is a security method that inspects devices as they attempt to connect to a network to determine if they are secure enough to be granted access. It's like a customs and immigration checkpoint at an airport, verifying a device's "credentials" and "health" before allowing it onto the network. NAC is a proactive security measure that goes beyond simple passwords, ensuring that every device and user connecting to the network is verified, compliant, and secure before being granted access.

✅ **Core NAC Inspection Mechanisms**
- **1. Port Security:**
  - **Concept:** Securing physical switch ports to prevent unauthorized devices from connecting.
  - **Method:** Can be configured to allow only a specific number of MAC addresses (or specific MAC addresses) on a given port.
- **2. MAC Filtering:**
  - **Concept:** Controlling network access based on a device's unique MAC address.
  - **Methods:**
    - **Allowlisting:** Only pre-approved MAC addresses can connect (more secure).
    - **Blocklisting:** Specific MAC addresses are blocked from connecting, while all others are allowed (less secure).
- **3. 802.1X Authentication:**
  - **Concept:** A robust authentication framework that provides port-based network access control.
  - **Components:**
    - **Supplicant:** The client device seeking access.
    - **Authenticator:** The network device the client connects to (e.g., switch, WAP).
    - **Authentication Server:** A centralized server (typically RADIUS) that validates the supplicant's credentials.
  - **Mechanism:** The authenticator acts as a gatekeeper, blocking all traffic except authentication requests until the authentication server validates the user/device.

✅ **NAC Enforcement Actions**
- **Quarantine Network:** If a device fails the NAC inspection (e.g., outdated antivirus, missing patches), it is placed in a restricted network segment (quarantine) where it can be remediated before being granted full access.
- **Agents:**
  - **Persistent Agent:** Software permanently installed on company-owned devices to continuously monitor compliance.
  - **Non-Persistent Agent:** A temporary, dissolvable agent run on guest or BYOD devices to perform a one-time compliance check, often initiated from a captive portal.

✅ **Types of Access Control Policies within NAC**
- **Time-based:** Restricts network access to specific times (e.g., business hours).
- **Location-based:** Restricts access based on the device's geographical location (geolocation).
- **Role-based (RBAC):** Grants permissions based on the user's job role within the organization (enforces the principle of least privilege).
- **Rule-based:** Grants or denies access based on a set of predefined rules (e.g., "device must have antivirus version X and all critical patches installed").