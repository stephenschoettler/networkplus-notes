## 💡 Multifactor Authentication (MFA) (OBJ 4.1)

Multifactor Authentication (MFA) is the process of authenticating (proving identity) using more than one method (at least two different categories). Its purpose is to enhance security beyond single-factor authentication (e.g., just a password).

✅ **Factors of Authentication (Categories)**
- **1. Something You Know (Knowledge Factor):**
  - **Examples:** Username, password, PIN, answers to personal questions.
  - **Weaknesses of Passwords:**
    - Default Credentials: Easily guessable.
    - Common Passwords: Widely used.
    - Weak/Short Passwords: Less than 8 characters, standard dictionary words, simple substitutions.
  - **Password Attacks:**
    - Dictionary Attack: Tries every word/phrase from a wordlist.
    - Brute Force Attack: Tries every possible combination until successful.
    - Hybrid Attack: Mix of dictionary and brute force.
  - **Defense:** Use long, strong passwords (at least 12 characters, mix of uppercase, lowercase, numbers, special characters).
- **2. Something You Have (Possession Factor):**
  - **Examples:** Smart card (with digital certificate), RSA key fob (generates rotating PIN), RFID tag (e.g., employee badge).
  - **MFA Example:** Smart card (something you have) + PIN (something you know).
- **3. Something You Are (Inherence Factor):**
  - **Examples:** Fingerprints, retina scans, voice prints.
  - **Nature:** Unique biological characteristics.
  - **Use:** Often in high-security environments (e.g., server room access) due to intrusiveness.
- **4. Something You Do (Action Factor):**
  - **Examples:** Signature (how you sign), drawing a pattern on a screen, saying a passphrase.
  - **Nature:** Unique actions.
  - **Use:** Can be combined with other factors (e.g., something you know) for MFA. Prone to error.
- **5. Somewhere You Are (Location Factor):**
  - **Examples:** Geotagging (GPS coordinates), geofencing (tracking device within/outside a defined area).
  - **Use:** Can be used to restrict access based on physical location.