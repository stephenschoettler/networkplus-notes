## 💡 Key Management (OBJ 4.3)

Key Management refers to how an organization generates, exchanges, stores, and uses encryption keys. The strength of any encryption relies on the security of its key. Proper key management is crucial for maintaining confidentiality.

✅ **Key Management Lifecycle**
- **1. Key Generation:**
  - Keys must be strong.
  - Often derived from user-created passwords (e.g., BitLocker, FileVault). A weak password leads to a weak key, compromising confidentiality even with strong algorithms.
- **2. Key Exchange:**
  - Secure exchange of keys is critical, especially for symmetric encryption.
  - Typically done using asymmetric (public-key) methods to encrypt the symmetric key for transmission over a network (e.g., Diffie-Hellman Algorithm used in VPNs, SSL/TLS).
- **3. Key Storage:**
  - Keys must be stored securely when not in use.
  - Like passwords, if a key is easily found, it can be used to decrypt data and breach confidentiality.
- **4. Key Use/Rotation:**
  - Keys should be changed (rotated) periodically.
  - Regular key rotation resets the "clock" on an attacker's efforts to break the key, providing additional security and confidentiality.