## 💡 Incorrect Wireless Configurations (OBJ. 5.4)
This section addresses common issues arising from incorrect wireless configurations, including problems with SSIDs, passphrases, and encryption protocol mismatches.

✅ **Incorrect Wireless Configurations**
- **1. SSID (Service Set Identifier) Issues:**
  - **Definition:** The human-readable name of a wireless network (e.g., "Starbucks Wi-Fi").
  - **Causes:**
    - **Typographical Errors:** Especially when manually typing the SSID (e.g., for network printers).
    - **Evil Twin Access Points:** A malicious AP mimicking a legitimate SSID to trick users.
  - **Troubleshooting:**
    - Always double-check the SSID for typos.
    - Be wary of SSIDs that are similar to yours but not legitimate.
- **2. Incorrect Passphrase Issues:**
  - **Definition:** The pre-shared key used for authentication and encryption on a wireless network.
  - **Causes:**
    - **Typographical Errors:** Entering the wrong password.
    - **Corrupted Drivers:** Wireless network adapter drivers can become corrupted, causing the passphrase to be incorrectly encrypted before sending.
  - **Troubleshooting:**
    - First, double-check the passphrase and re-enter it carefully.
    - If the issue persists, try reinstalling the wireless network adapter's drivers.
- **3. Encryption Protocol Mismatch Issues:**
  - **Encryption Protocols:**
    - WEP: Uses RC4 encryption.
    - WPA: Uses TKIP encryption.
    - WPA2: Uses AES encryption (default).
  - **Problem:** Client and Access Point (AP) are configured to use different encryption protocols, resulting in a "Network security key mismatch" error.
  - **Troubleshooting:**
    - **Manually Change Protocol:** Attempt to manually configure the client's wireless network settings to match the AP's encryption protocol.
    - **Disable Third-Party Antivirus:** Some antivirus software can interfere with wireless encryption protocols. Temporarily disable it to test.
    - **Reinstall Wireless Drivers:** Corrupted drivers can also cause this issue; reinstalling them may resolve it.
- **General Tip:** Ensure the correct SSID, passphrase, and encryption protocol are used. If problems persist despite correct settings, it may indicate a deeper issue with the operating system or network drivers.