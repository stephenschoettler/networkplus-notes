## 💡 Email Ports and Protocols (OBJ 1.4)

Email Ports and Protocols govern the transmission and retrieval of emails. Always choose the secure variants (SMTPS, POP3S, IMAPS) when configuring email systems to protect sensitive data. Understand the difference between POP3 (downloads and deletes, single device focus) and IMAP (manages on server, multiple device sync).

✅ **1. SMTP (Simple Mail Transfer Protocol)**
- **Purpose:** Standard protocol for **sending emails**.
- **Port:** 25 (TCP).
- **Note:** Used by email servers to relay messages. Only for sending, not receiving.
- **Insecure:** Transmits in plain text.

✅ **2. SMTPS (SMTP Secure)**
- **Purpose:** Secure variant of SMTP, using SSL/TLS to create an encrypted tunnel for SMTP traffic.
- **Ports:** 465 or 587 (TCP).
- **Importance:** Encrypts email messages during transit, protecting them from unauthorized access.

✅ **3. POP3 (Post Office Protocol Version 3)**
- **Purpose:** Retrieves emails from a remote server to a local client.
- **Port:** 110 (TCP).
- **Functionality:** Traditionally downloads messages and deletes them from the server. Newer versions allow keeping a copy on the server, but read/delete status is not synchronized across devices.
- **Use Case:** Best for accessing email from a single device.
- **Insecure:** Transmits in plain text.

✅ **4. POP3S (POP3 Secure)**
- **Purpose:** Secure variant of POP3, using SSL/TLS to encrypt POP3 data.
- **Port:** 995 (TCP).

✅ **5. IMAP (Internet Message Access Protocol)**
- **Purpose:** Offers more flexibility for receiving emails; allows managing emails directly on the server.
- **Port:** 143 (TCP).
- **Functionality:** Synchronizes messages across multiple devices (read, delete, send status are consistent).
- **Use Case:** Ideal for users who access email from multiple devices (work computer, laptop, tablet, smartphone).
- **Insecure:** Transmits in plain text.

✅ **6. IMAPS (IMAP Secure)**
- **Purpose:** Secure variant of IMAP, using SSL/TLS to encrypt IMAP data.
- **Port:** 993 (TCP).