## 💡 On-Path Attack (OBJ 4.2)

An On-Path Attack (also known as Man-in-the-Middle or Interception Attack) is an attack where the attacker logically places their workstation between two communicating hosts to transparently capture, modify, and/or relay their communications. The goal is to intercept authorization packets, take over sessions, and read/modify data.

✅ **Methods of Conducting On-Path Attacks**
- ARP poisoning
- DNS poisoning
- Introducing a rogue wireless access point (Evil Twin)
- Introducing a rogue hub or switch

✅ **Types of Attacks Performed in an On-Path Position**
- **1. Replay Attack:**
  - **Mechanism:** Valid data (e.g., authentication handshake) is captured by the attacker and then repeated (replayed) later to gain unauthorized access.
  - **Defense:** Anti-replay mechanisms (e.g., sequence numbers, timestamps).
- **2. Relay Attack:**
  - **Mechanism:** The attacker becomes an active proxy between the two communicating hosts, reading or modifying communications in real-time.
  - **Impact:** Breaches confidentiality (attacker sees data) and integrity (attacker can modify data, e.g., changing transaction amounts).

✅ **Attacks Against Encryption in On-Path Scenarios**
- **SSL Stripping (or HTTPS Stripping):**
  - **Mechanism:** Attacker tricks the client/server into downgrading an HTTPS connection to an unencrypted HTTP connection.
  - **Effect:** Strips out the encryption layer, allowing the attacker to capture and read all data in plain text.
- **Downgrade Attack:**
  - **Mechanism:** Attacker forces a client or server to abandon a higher security mode (e.g., TLS 1.3) in favor of a lower, less secure mode (e.g., SSL 2.0).
  - **Effect:** Communication remains encrypted, but with a weaker algorithm that is easier for the attacker to crack in real-time.
  - **Scope:** Not limited to SSL/TLS; can apply to Wi-Fi, VPNs, or any protocol that negotiates security levels.
- **Defense:** Strong encryption (TLS 1.3), HSTS (HTTP Strict Transport Security) to prevent SSL stripping, and proper configuration to prevent downgrade attacks.