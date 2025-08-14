## 💡 Authentication Methods (OBJ 4.1)

Authentication is the process of determining whether someone or something is, in fact, who they claim to be.

✅ **1. Local Authentication**
- **Mechanism:** Username and password stored and verified directly on the local device (e.g., personal laptop login).
- **Security:** Single-factor authentication.

✅ **2. LDAP (Lightweight Directory Access Protocol)**
- **Mechanism:** Centralized directory service (database) used to store information about users, groups, and objects. Validates username/password against the LDAP server.
- **Ports:** 389/TCP (plain text), 636/TCP (LDAPS - secure using SSL/TLS).
- **Cross-Platform:** Works with Unix, Linux, Mac, Windows.
- **Microsoft Implementation:** Active Directory (AD) is Microsoft's implementation of LDAP.

✅ **3. Kerberos**
- **Mechanism:** Authentication protocol providing secure authentication services over an insecure network, primarily within Windows domain environments. Uses a system of "tickets" (Ticket Granting Ticket - TGT, Service Ticket) to avoid sending passwords over the network.
- **Mutual Authentication:** Provides two-way authentication.
- **Key Distribution Center (KDC):** Domain Controller acts as KDC (authentication and ticket granting).
- **Port:** 88/TCP.
- **Single Point of Failure:** KDC can be a single point of failure; redundancy (primary/secondary DCs) is crucial.

✅ **4. Single Sign-On (SSO)**
- **Mechanism:** Allows users to authenticate once with a single set of credentials to access multiple applications and resources.
- **Pros:** Simplifies user experience, reduces password fatigue, easier user/password management for IT.
- **Cons:** If master credentials are compromised, attacker gains access to all linked resources (like a master key).
- **Security Enhancement:** Best used with Multi-Factor Authentication (MFA).

✅ **5. SAML (Security Assertion Markup Language)**
- **Mechanism:** XML-based data format used to exchange authentication and authorization information between a client and a service. Often used with SOAP.
- **Purpose:** Provides SSO and federated identity management. Allows a service provider to trust a user's identity from an identity provider (e.g., logging into a website using your Google account).
- **Roles:** Service Provider, User Agent (web browser), Identity Provider.

✅ **6. RADIUS (Remote Authentication Dial-In User Service)**
- **Mechanism:** Centralized administration for dial-up, VPN, and wireless (802.1x, EAP) authentication. Client-server protocol.
- **Protocol:** Uses UDP (fast).
- **Ports:** 1812/UDP (authentication), 1813/UDP (accounting). Some proprietary versions use 1645/1646.
- **Cross-Platform:** Considered a cross-platform standard.

✅ **7. TACACS+ (Terminal Access Controller Access Control System Plus)**
- **Mechanism:** Cisco proprietary protocol for authentication, authorization, and accounting (AAA). Can act as an authenticator in 802.1x networks.
- **Protocol:** Uses TCP (slower than RADIUS).
- **Pros:** More security features, independent AAA processes, supports all major network protocols.
- **Cons:** Proprietary to Cisco; requires all Cisco devices in the network.

✅ **8. Time-Based Authentication (TOTP - Time-Based One-Time Password)**
- **Mechanism:** Generates a temporary, dynamic password/token valid for a short period (e.g., 30-60 seconds) by combining a shared secret key with the current timestamp.
- **Use:** Commonly used as part of Multi-Factor Authentication (MFA).
- **Pros:** Significantly enhances security; resistant to replay attacks (stolen passwords expire quickly).
- **Implementation:** Software (Google/Microsoft Authenticator), hardware tokens (RSA Key Fob, YubiKey), email/SMS codes.