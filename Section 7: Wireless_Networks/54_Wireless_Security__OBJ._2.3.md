## 💡 Wireless Security (OBJ 2.3)

Wireless Security aims to protect wireless networks from unauthorized access and to secure data transmitted over the airwaves.

✅ **Wireless Authentication Methods**
- **1. Pre-Shared Key (PSK):**
  - **Concept:** A single, shared password (passphrase) is used by all devices to connect to the network.
  - **Use Case:** Common in home and small office networks.
  - **Limitations:**
    - **Scalability:** Difficult to manage in large environments; if one person leaves, the key must be changed for everyone.
    - **Accountability:** No individual user accountability, as everyone uses the same key.
- **2. Enterprise Authentication (802.1X):**
  - **Concept:** Each user authenticates with their own unique credentials (e.g., username/password, digital certificate).
  - **Mechanism:** Uses an authentication server, typically **RADIUS**, to manage user credentials.
  - **Use Case:** Large office and enterprise environments.
  - **Benefits:** Provides individual user accountability, better security, and centralized key management.

✅ **Wireless Security & Encryption Protocols**
- **1. WEP (Wired Equivalent Privacy):**
  - **Status:** ⚠️ **Obsolete and insecure. NEVER use.**
  - **Vulnerabilities:** Used the weak RC4 encryption algorithm and had a critical flaw in its 24-bit Initialization Vector (IV), making it easy to crack in minutes.
- **2. WPA (Wi-Fi Protected Access):**
  - **Status:** ⚠️ **Outdated and insecure.**
  - **Improvements over WEP:** Introduced **TKIP (Temporal Key Integrity Protocol)** to replace the flawed IV and a Message Integrity Check (MIC) for data integrity.
  - **Vulnerability:** Still used the weak RC4 encryption algorithm, and TKIP was found to be vulnerable.
- **3. WPA2 (Wi-Fi Protected Access 2):**
  - **Status:** ✅ **Still widely used and considered secure for most use cases.**
  - **Improvements over WPA:**
    - Replaced RC4 with the strong **AES (Advanced Encryption Standard)** encryption algorithm.
    - Replaced TKIP/MIC with **CCMP (Counter Mode with Cipher Block Chaining Message Authentication Code Protocol)** for enhanced integrity and confidentiality.
  - **Modes:** Supports both **Personal (PSK)** and **Enterprise (802.1X)** modes.
- **4. WPA3 (Wi-Fi Protected Access 3):**
  - **Status:** ✅ **The most secure and current standard.**
  - **Improvements over WPA2:**
    - **SAE (Simultaneous Authentication of Equals):** Replaces PSK with a more secure handshake method (based on the Dragonfly key exchange) that is resistant to offline dictionary attacks.
    - **Enhanced Encryption:** Supports stronger 192-bit and 256-bit AES encryption in enterprise mode.
    - **Forward Secrecy:** If a session key is compromised, past communications remain secure.
- **5. WPS (Wi-Fi Protected Setup):**
  - **Concept:** A standard aimed at simplifying the connection process, often using a push-button or an 8-digit PIN.
  - **Status:** ⚠️ **Highly insecure and should be disabled.**
  - **Vulnerability:** The 8-digit PIN is validated in two 4-digit halves, drastically reducing the number of possible combinations and making it vulnerable to brute-force attacks.

✅ **Exam Quick Reference**
- **Open:** No security.
- **WEP:** Think **IV** (vulnerability).
- **WPA:** Think **TKIP** and **RC4**.
- **WPA2:** Think **CCMP** and **AES**.
- **WPA3:** Think **SAE** (replaces PSK).
- **WPS:** Think **PIN** (vulnerability).
- **PSK:** Think **Personal Mode**.
- **Enterprise Mode:** Think **802.1X** and **RADIUS**.