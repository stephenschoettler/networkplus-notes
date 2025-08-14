## 💡 Public Key Infrastructure (PKI) (OBJ 4.1)

PKI is an entire system of hardware, software, policies, procedures, and people based on asymmetric encryption. Its purpose is to manage digital keys and certificates to facilitate secure data transfer, authentication, and encrypted communications over networks (e.g., HTTPS).

✅ **Relationship with Public Key Cryptography**
- **Public Key Cryptography:** Refers specifically to the asymmetric encryption and decryption process (using public/private key pairs).
- **PKI:** The overarching system that creates, manages, and validates these key pairs, and ensures their trustworthiness. Public key cryptography is just one part of PKI.

✅ **How it Works (Simplified HTTPS Example)**
- **1. Web browser requests server's public key from a trusted Certificate Authority (CA).**
- **2. Browser generates a random shared secret key (for symmetric encryption).**
- **3. Browser encrypts the shared secret key using the server's public key.**
- **4. Encrypted shared secret is sent to the server.**
- **5. Server decrypts the shared secret using its private key (only the server has this).**
- **6. Both browser and server now have the shared secret key.**
- **7. They switch to symmetric encryption (e.g., AES) using the shared secret key to create a secure, encrypted tunnel for bulk data transfer.**
- **8. This process provides confidentiality (data is encrypted) and authentication (browser trusts the server's identity via its public key/certificate).**

✅ **Key Escrow**
- **Definition:** A process where a secure copy of a user's private key is held by a third party (escrow agent).
- **Purpose:** Allows retrieval of keys if lost (e.g., employee leaves, private key is lost), ensuring encrypted data remains accessible to the organization. Also used in legal investigations.
- **Controversy/Risk:** If the escrow keys are compromised by a malicious actor, it could lead to decryption of vast amounts of data. Requires extremely secure storage and strict access regulations (e.g., separation of duties).