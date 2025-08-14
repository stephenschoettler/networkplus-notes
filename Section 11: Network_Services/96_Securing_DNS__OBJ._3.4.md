## 💡 Securing DNS (OBJ 3.4)

DNS is a critical network component; if compromised, attackers can redirect users to malicious sites (e.g., phishing). Early DNS design lacked security, making it susceptible to various attacks.
**Overall Benefits of Secure DNS:**
- **Integrity:** Ensures DNS data is authentic and untampered.
- **Privacy:** Protects user browsing habits from monitoring (DoH, DoT).
- **Trust:** Safeguards trust in the digital ecosystem by ensuring users reach intended destinations.
**Implementation Considerations:**
- Requires collaborative effort from website owners (DNSSEC) and ISPs/organizations (DoH/DoT support).
- Balancing privacy with local network control (especially with DoH).

✅ **Key DNS Security Measures**
- **1. DNSSEC (DNS Security Extensions)**
  - **Purpose:** Provides a **digital tamper-proof seal** for DNS data. Ensures the information received is authentic and has not been altered.
  - **Mechanism:** Uses **cryptographic signatures** attached to DNS data, verified against a chain of trust.
  - **Benefit:** Prevents DNS spoofing and cache poisoning by detecting falsified DNS records.
  - **Limitation:** Does **NOT** encrypt DNS data; eavesdroppers can still see DNS queries.
- **2. DNS over HTTPS (DoH)**
  - **Purpose:** Encrypts DNS queries.
  - **Mechanism:** Sends DNS queries through the **HTTPS protocol** (the same protocol used for secure web browsing).
  - **Benefits:**
    - **Encryption:** Protects the content of DNS queries from eavesdropping.
    - **Traffic Blending:** Blends DNS traffic with regular HTTPS web traffic, making it harder for attackers to identify and monitor DNS requests.
    - **Privacy:** Prevents DNS snooping (monitoring DNS queries to infer user browsing habits).
  - **Consideration:** Can shift DNS resolution control from local network/ISP to a third-party DoH provider.
- **3. DNS over TLS (DoT)**
  - **Purpose:** Encrypts DNS queries.
  - **Mechanism:** Encapsulates DNS traffic inside a **Transport Layer Security (TLS) tunnel**.
  - **Benefits:**
    - **Encryption:** Provides privacy for DNS data in transit.
    - **Privacy:** Prevents DNS snooping.
    - **Difference from DoH:** Uses a dedicated TLS port (853) rather than blending with general web traffic.