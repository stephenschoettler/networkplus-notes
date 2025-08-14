## 💡 Other Network Service Ports and Protocols (OBJ 1.4)

This section covers other important network service ports and protocols. Memorize the protocol, its purpose, and its associated port numbers. Understand why LDAPS is preferred over LDAP.

✅ **NTP (Network Time Protocol)**
- **Purpose:** Synchronizes the clocks of computers over a network.
- **Importance:** Crucial for consistent time-stamping, transaction logging, security protocols, and system coordination (e.g., domain login, encryption/decryption functions).
- **Port:** 123 (UDP).

✅ **SIP (Session Initiation Protocol)**
- **Purpose:** Initiates, maintains, and terminates real-time sessions involving voice, video, messaging, and other communication services.
- **Common Use:** Voice over IP (VoIP) applications.
- **Ports:**
  - 5060 (UDP/TCP): For unencrypted signaling.
  - 5061 (TCP): For encrypted signaling (using TLS).

✅ **LDAP (Lightweight Directory Access Protocol)**
- **Purpose:** Accessing and maintaining distributed directory information services over an IP network.
- **Common Use:** Looking up user information (email, phone, department) in internal company directories.
- **Port:** 389 (TCP/UDP).
- **Insecure:** Transmits information in plain text.

✅ **LDAPS (Lightweight Directory Access Protocol Secure)**
- **Purpose:** Secure version of LDAP, encrypted with SSL/TLS.
- **Importance:** Used for protecting sensitive data during directory service transactions.
- **Port:** 636 (TCP).
- Ensures data is securely encrypted before transmission.