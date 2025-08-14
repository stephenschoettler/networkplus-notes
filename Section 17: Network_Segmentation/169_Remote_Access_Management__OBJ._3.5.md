## 💡 Remote Access Management (OBJ 3.5)

Remote Access Management allows clients to access servers or network devices remotely. Administrators use these to configure network devices.

✅ **Remote Access Technologies/Protocols**
- **1. Telnet:**
  - **Port:** 23/TCP.
  - **Function:** Sends text-based commands to remote devices.
  - **Security:** Highly Insecure. Sends everything in plain text. Never use for secure devices.
- **2. Secure Shell (SSH):**
  - **Port:** 22/TCP.
  - **Function:** Works like Telnet but encrypts all communication.
  - **Security:** Secure. Always use SSH for configuring network devices via CLI.
- **3. Remote Desktop Protocol (RDP):**
  - **Port:** 3389/TCP.
  - **Function:** Microsoft proprietary protocol providing a graphical interface (GUI) to connect to Windows servers/clients.
  - **Security:** RDP itself is not considered secure without tunneling.
- **4. Remote Desktop Gateway (RDG):**
  - **Function:** A Windows server role that creates a secure, encrypted connection (SSL/TLS) to RDP servers.
  - **Purpose:** Secures RDP connections without needing a separate VPN. Provides centralized access control and monitoring.
- **5. Virtual Network Computing (VNC):**
  - **Port:** 5900/TCP.
  - **Function:** Cross-platform graphical remote access (Linux, OS X, Windows). Similar to RDP.
  - **Use:** Often used with thin client architectures and VDI.
- **6. Virtual Desktop Infrastructure (VDI):**
  - **Function:** Hosts desktop environments on a centralized server (desktop virtualization).
  - **Access:** Via web browser or specialized thin client devices.
  - **Cloud Equivalent:** Desktop as a Service (DaaS).

✅ **Management Approaches**
- **1. In-Band Management:**
  - **Definition:** Managing devices over the same network that the devices are configured to operate on (e.g., SSH/Telnet to a router from a workstation on the LAN).
  - **Risk:** If the production network is compromised, management access can also be compromised.
- **2. Out-of-Band Management (OOB):**
  - **Definition:** Using an alternate, separate network or direct connection to manage devices.
  - **Best Practice:** Considered more secure.
  - **Examples:** Dedicated management network, direct console connection.
  - **Purpose:** Provides separation of data, prevents attackers from gaining control of management interfaces if the production network is breached. Requires additional equipment/configuration.

✅ **APIs (Application Programming Interfaces)**
- **Function:** Set of protocols/routines for building and interacting with software applications. Acts as an intermediary.
- **Use in Remote Management:** Allows automated administration, management, and monitoring of cloud services and applications.
- **Communication:** Typically uses REST or SOAP.