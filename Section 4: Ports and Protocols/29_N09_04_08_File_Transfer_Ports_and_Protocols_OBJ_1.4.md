## 💡 File Transfer Ports and Protocols (OBJ 1.4)

File Transfer Ports and Protocols are specialized rules and procedures for transmitting files across networks, operating on designated ports. Understand the security implications of each protocol. FTP and TFTP are insecure; SFTP is secure. SMB is primarily for LAN file sharing. Memorize their ports.

✅ **1. FTP (File Transfer Protocol)**
- **Purpose:** Transfers files between a client and a server.
- **Ports:**
  - 20 (TCP): Data transfer.
  - 21 (TCP): Control commands (setting up transfer, authentication).
- **Insecure:** Transmissions are **not encrypted** (plain text), making usernames/passwords vulnerable to interception.

✅ **2. SFTP (SSH File Transfer Protocol / Secure File Transfer Protocol)**
- **Purpose:** Securely transfers files, addressing FTP's security concerns.
- **Port:** 22 (TCP) - operates over SSH (Secure Shell).
- **Features:** Tunnels FTP through an encrypted SSH connection, providing confidentiality and integrity for file transfers.

✅ **3. TFTP (Trivial File Transfer Protocol)**
- **Purpose:** Simpler, more basic version of FTP, designed for sending files when minimal security is sufficient.
- **Port:** 69 (UDP).
- **Features:** No user authentication, no directory browsing.
- **Common Use:** Booting diskless workstations, network devices, VoIP phones (for downloading configuration files or firmware).

✅ **4. SMB (Server Message Block)**
- **Purpose:** Network file sharing protocol allowing applications to read/write files and request services from server programs.
- **Port:** 445 (TCP).
- **Common Use:** Predominantly used for **Windows file sharing** within local area networks (LANs).
- **Note:** Not typically used for internet-based file transfers like FTP/SFTP. Samba is a cross-platform implementation for Linux systems.