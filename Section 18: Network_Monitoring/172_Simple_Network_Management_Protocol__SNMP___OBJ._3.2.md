## 💡 Simple Network Management Protocol (SNMP) (OBJ 3.2)

SNMP is an Internet protocol for collecting and organizing information about managed devices on IP networks, and for modifying that information to change device behavior. Managed devices include any device that can communicate with an SNMP manager (routers, switches, firewalls, printers, servers, clients).

✅ **Architecture**
- **SNMP Manager:** A machine (usually a server) running the SNMP protocol to collect and process information.
- **SNMP Agents:** Network devices running a background service to collect data and send it to the manager.

✅ **SNMP Message Types**
- **1. Set Request:** Manager to agent request to change the value of a variable.
- **2. Get Request:** Manager to agent request to retrieve the value of a variable.
- **3. Trap Message:** Asynchronous notification sent from an agent to the manager without being requested.
  - Used for real-time event/alarm notifications (e.g., uptime, config changes, link down).
  - **Granular Traps:** Send a unique Object Identifier (OID) for each message. OIDs are defined in the Management Information Base (MIB), which describes the structure of management data. This saves bandwidth.
  - **Verbose Traps:** Contain all information about an alert/event as a payload, using more resources.
  - Data is sent as variable bindings (key-value pairs).

✅ **SNMP Versions and Security**
- **SNMPv1 & SNMPv2:**
  - Use a "community string" as a shared secret key for access.
  - **Major Security Flaw:** Community strings are sent/stored in plain text, making them highly insecure and vulnerable to attack.
  - Default community strings ("public" for read-only, "private" for read-write) are a huge risk.
- **SNMPv3:**
  - Most Secure Version.
  - **Security Enhancements:** Adds Integrity, Authentication, and Confidentiality.
    - **Integrity:** Hashing messages before transmission to prevent alteration.
    - **Authentication:** Validating the source of messages.
    - **Confidentiality:** Encryption (originally DES, now relies on device firmware for stronger algorithms like 3DES/AES).
    - **Authorization:** Groups SNMP components into entities with different authorizations (read, write, read-write) to increase security.
  - **Recommendation:** Always use SNMPv3 for its enhanced security features.