## 💡 Understanding Digital Certificates (OBJ 4.1)

Digital Certificates are used to verify the identity of websites/servers (and other entities) and to secure communication (e.g., HTTPS). You can view them by clicking the padlock icon next to the URL in a web browser. Both RSA and ECC provide high levels of security. The choice often depends on the device's processing capabilities and the need for efficiency (ECC for mobile, RSA for desktop).

✅ **Key Information Contained in a Digital Certificate**
- **Subject:** Who the certificate was issued to (e.g., Google LLC, Apple Inc.).
- **Issuer:** The Certificate Authority (CA) that issued the certificate (e.g., Google Trust Services, DigiCert).
- **Validity Period:** "Valid from" and "Valid to" dates (ensures the certificate is not expired).
- **Public Key Information:** Contains the public key used for encryption.
- **Signature Algorithm:** Used for integrity (e.g., SHA-256).
- **Encryption Algorithm:** Used for key exchange and data encryption (e.g., RSA, ECC).
- **Key ID/Fingerprint:** Unique identifiers for the certificate.

✅ **Common Encryption Algorithms in Certificates**
- **1. RSA (Rivest–Shamir–Adleman):**
  - **Characteristics:** Older, widely used asymmetric encryption algorithm.
  - **Key Size:** Typically larger key sizes (e.g., 2048 bits) for strong security.
  - **Use Case:** Favored for desktop computers due to higher processing power.
- **2. ECC (Elliptic Curve Cryptography):**
  - **Characteristics:** Newer asymmetric encryption algorithm.
  - **Key Size:** Smaller key sizes (e.g., 256 bits) provide equivalent security to much larger RSA keys.
  - **Use Case:** Favored for mobile and low-power devices due to less computational overhead.