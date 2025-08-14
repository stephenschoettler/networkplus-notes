## 💡 Encryption (OBJ 4.1)

Encryption is a security method where information is encoded so it can only be accessed or decrypted by a user with the correct security key. Unencrypted data (Clear Text / Plain Text) is easily viewable or accessible and vulnerable to interception, while encrypted data (Cipher Text) is scrambled and unreadable without the proper key. Encryption acts as a risk mitigation for access controls; even if an attacker bypasses other controls and gains access to encrypted data, they cannot read it without the key, thus protecting confidentiality. Data constantly moves between these three states, so it's crucial to consider how data will be protected (encrypted) during each state to ensure end-to-end confidentiality.

✅ **Three States of Data**
- **1. Data at Rest:**
  - **Definition:** Any data stored in memory, on a hard drive, or on a storage device (e.g., files on an external hard drive).
  - **Protection:** Full disk encryption (e.g., BitLocker, FileVault), folder encryption, file encryption, database encryption.
  - **Goal:** Ensure confidentiality of stored data.
- **2. Data in Motion (Data in Transit):**
  - **Definition:** Any data currently moving from one computer to another over a network, or within different parts of the same computer system (e.g., hard disk to memory).
  - **Protection:** Transport encryption protocols (e.g., TLS/SSL for web traffic, IPSec/L2TP for VPNs, WPA2/AES for wireless connections).
  - **Goal:** Maintain confidentiality as data travels across systems or networks.
- **3. Data in Use (Data in Processing):**
  - **Definition:** Any data that has been read into memory or is currently inside the processor, being worked on or manipulated. This is active, non-persistent data (e.g., in RAM, CPU caches/registers).
  - **Protection:** Modern processors (AMD, Intel) involve secure processing mechanisms with encryption and integrity checks.
  - **Goal:** Protect data while it's actively being used by the computer's CPU.