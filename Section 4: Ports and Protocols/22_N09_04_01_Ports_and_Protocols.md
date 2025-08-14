## 💡 Ports and Protocols

A **port** is a virtual point of entry or exit for communications used by software applications to exchange information. A **protocol** is a set of rules and conventions for data exchange between network devices, ensuring structured and predictable data transmission. Ports and protocols are essential building blocks for efficient and secure data sharing.

✅ **Port Ranges**
- **Well-known Ports:** 0 to 1023 (e.g., HTTP 80, HTTPS 443).
- **Registered Ports:** 1024 to 49,151.
- **Dynamic or Private Ports:** 49,152 to 65,535.

✅ **Key Protocols and Services**
- **TCP (Transmission Control Protocol):** Reliable, connection-oriented.
- **UDP (User Datagram Protocol):** Unreliable, connectionless.
- **ICMP (Internet Control Message Protocol):** Used for network diagnostics (e.g., Ping).
- **Web Ports and Protocols:**
  - **HTTP (Hypertext Transfer Protocol):** 80 (unencrypted web traffic).
  - **HTTPS (Hypertext Transfer Protocol Secure):** 443 (secure, encrypted web traffic).
- **Email Ports and Protocols:**
  - **SMTP (Simple Mail Transfer Protocol):** 25 (sending emails).
  - **SMTPS (Secure SMTP):** 587 (secure sending emails).
  - **POP3 (Post Office Protocol version 3):** 110 (receiving emails, downloads to client).
  - **IMAP (Internet Message Access Protocol):** 143 (receiving emails, keeps on server).
- **File Transfer Ports and Protocols:**
  - **FTP (File Transfer Protocol):** 20 (data), 21 (control) (unencrypted file transfer).
  - **SFTP (Secure File Transfer Protocol):** 22 (secure file transfer over SSH).
  - **TFTP (Trivial File Transfer Protocol):** 69 (simple, unauthenticated file transfer).
- **Remote Access Ports and Protocols:**
  - **SSH (Secure Shell):** 22 (secure remote access).
  - **Telnet:** 23 (insecure remote access).
  - **RDP (Remote Desktop Protocol):** 3389 (remote desktop access).
- **Networking Service Ports and Protocols:**
  - **DNS (Domain Name System):** 53 (translates domain names to IP addresses).
  - **DHCP (Dynamic Host Configuration Protocol):** 67 (server), 68 (client) (assigns IP addresses automatically).
  - **SQL (Structured Query Language):** 1433 (database communication).
  - **SNMP (Simple Network Management Protocol):** 161 (agent), 162 (manager) (network device management).
  - **Syslog:** 514 (logging system messages).
- **Other Network Service Ports and Protocols:**
  - **NTP (Network Time Protocol):** 123 (time synchronization).
  - **SIP (Session Initiation Protocol):** 5060 (UDP/TCP), 5061 (TCP/TLS) (voice/video communication).
  - **LDAP (Lightweight Directory Access Protocol):** 389 (directory services, insecure).
  - **LDAPS (LDAP Secure):** 636 (secure directory services).

✅ **Nmap**
- A network mapping tool used to scan for open ports and protocols.