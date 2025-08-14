## 💡 Remote Access Ports and Protocols (OBJ 1.4)

Remote Access Ports and Protocols enable management of systems and networks from remote locations. Prioritize SSH over Telnet for security. Understand that SSH and Telnet are primarily text-based, while RDP provides a graphical interface. Memorize their respective port numbers.

✅ **1. SSH (Secure Shell)**
- **Purpose:** Secure remote login and other secure network services over an unsecure network.
- **Port:** 22 (TCP).
- **Features:** Provides a secure, encrypted channel (SSH tunnel) for strong authentication and encrypted data communications.
- **Usage:** Widely used by network administrators for secure command-line based management of web and server applications.
- **Benefit:** Operates over unsecured networks like the internet without exposing data.

✅ **2. Telnet**
- **Purpose:** One of the earliest remote login protocols. Allows remote login to another computer on the same network.
- **Port:** 23 (TCP).
- **Insecure:** Transfers data in **plain text**, making it susceptible to eavesdropping and on-path attacks due to lack of encryption.
- **Replacement:** Largely replaced by SSH due to security vulnerabilities. Should generally not be used unless absolutely necessary for legacy equipment that doesn't support SSH.

✅ **3. RDP (Remote Desktop Protocol)**
- **Purpose:** Proprietary Microsoft protocol providing users with a **graphical user interface (GUI)** to connect to another computer over a network.
- **Port:** 3389 (TCP).
- **Features:** Allows remote control of a Windows system as if sitting in front of it. Supports encryption, smart card authentication, and bandwidth reduction.
- **Usage:** Essential for secure graphical access to Windows-based systems remotely.