## 💡 The CIA Triad (OBJ 4.1)

The CIA Triad is a fundamental model in information security that defines the three core principles for securing data and systems. Networks are fundamentally not secure by default; security is "bolted on."

✅ **1. Confidentiality (C)**
- **Concern:** Keeping data safe and private; preventing unauthorized disclosure.
- **Mechanism:** Encryption (symmetric and asymmetric).
  - **Symmetric Encryption:** Uses the same key for both encryption and decryption. Pros: Fast. Con: Key management is challenging.
  - **Asymmetric Encryption (Public Key Cryptography):** Uses a pair of keys (public and private). Pros: Solves key distribution. Con: Slower.
  - **Common Use:** Asymmetric for key exchange, then switch to faster symmetric for bulk data transfer.

✅ **2. Integrity (I)**
- **Concern:** Ensuring data has not been modified (altered, tampered with) in storage or in transit. Verifies the source of traffic.
- **Mechanism:** Hashing.
  - **Hashing:** An algorithm runs a string of data to create a fixed-size hash. If hashes match, integrity is confirmed.

✅ **3. Availability (A)**
- **Concern:** Measuring the accessibility of data and systems. Can users get to the data/services when and where they want?
- **Mechanism:** Designing redundant networks, high availability solutions.
- **Compromise:** Can be compromised by:
  - **Attacks:** DoS/DDoS.
  - **System Failures:** Hardware/software.
  - **Environmental Factors:** Power outages, floods.
  - **Overload:** Even legitimate traffic can cause DoS.