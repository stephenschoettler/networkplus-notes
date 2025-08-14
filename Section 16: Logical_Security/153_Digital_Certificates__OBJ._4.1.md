## 💡 Digital Certificates (OBJ 4.1)

A digital certificate is a digitally-signed electronic document that binds a public key with a user's (person, server, workstation, device) identity. It commonly uses the X.509 protocol standard within PKI and contains owner/user information (name, organization, public key) and Certificate Authority (CA) information.

✅ **Types of Digital Certificates**
- **1. Wildcard Certificate:**
  - Allows all subdomains (e.g., `www.example.com`, `mail.example.com`) to use the same public key certificate.
  - **Pros:** Easy to manage, cost-effective (one certificate for many subdomains).
  - **Cons:** If compromised, all associated subdomains are affected.
- **2. Subject Alternative Name (SAN) Certificate:**
  - Used when multiple distinct domain names (e.g., `diontraining.com`, `jasondion.com`) need to be covered by one certificate.
  - Modified in the SAN field of the certificate.
- **3. Single-Sided Certificate:**
  - Only the server identifies itself to the client using its digital certificate. Client is not required to authenticate with a certificate.
  - Common for most websites (e.g., HTTPS browsing).
- **4. Dual-Sided Certificate:**
  - Both the server and the user (client) validate each other using certificates.
  - **Pros:** Better security.
  - **Cons:** Requires more processing power, typically used in high-security environments.
- **5. Self-Signed Certificate:**
  - Signed by the same entity whose identity it's certifying (entity vouches for itself).
  - **Pros:** Provides encryption.
  - **Cons:** Does not offer the same level of trust as third-party certificates (no external verification). Web browsers will issue warnings.
  - **Use:** Testing environments, closed systems, non-production systems where trust is already established.
- **6. Third-Party Certificate:**
  - Issued and signed by a trusted Certificate Authority (CA).
  - CA root certificates are embedded in major web browsers/OS, making certificates issued by them inherently trusted.
  - Preferred for publicly-facing websites/applications due to higher trust and security.

✅ **Public Key Infrastructure (PKI) Elements**
- **1. Root of Trust (Chain of Trust):**
  - **Concept:** Where a certificate's authenticity is validated by tracing it back to a known and trusted root CA (like a family tree).
  - The root CA is the highest level of trust.
- **2. Certificate Authority (CA):**
  - Trusted third-party that issues and signs digital certificates.
  - Maintains a publicly accessible copy of users' public keys.
- **3. Registration Authority (RA):**
  - Requests identifying information from the user and forwards the certificate request to the CA.
- **4. Certificate Signing Request (CSR):**
  - A block of encoded text that contains information about the entity requesting the certificate (organization name, domain, locality, country) and its public key.
  - The private key associated with the request remains with the requester and is never sent to the CA.
- **5. Certificate Revocation List (CRL):**
  - An online list maintained by each CA of digital certificates that have been revoked (e.g., due to compromise).
  - Browsers/systems check the CRL before trusting a certificate.
- **6. Key Escrow Agents:**
  - Holds a secure copy of a user's private key in case the user loses it.
  - Used when data loss is unacceptable. Requires strong protection and separation of duties.
- **7. Key Recovery Agents:**
  - Specialized software that allows the restoration of a lost or corrupted key. Acts as a backup for CA keys.
- **Importance of Trust:** If a root CA is compromised, all certificates issued by that CA are compromised and must be revoked/reissued.