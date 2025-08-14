## 💡 Understanding Wireless Security (OBJ 2.3)

This lesson demonstrates how to configure a typical SOHO (Small Office/Home Office) wireless router for better security.

✅ **Key Wireless Security Settings & Best Practices**
- **1. Disable SSID Broadcast:**
  - **What it does:** Prevents the router from publicly advertising the network name (SSID).
  - **Why:** Makes it slightly harder for casual attackers to discover your network. Users must manually type in the SSID to connect.
  - **Exam Tip:** CompTIA considers this a security best practice.
- **2. Enable Wireless Isolation (AP Isolation):**
  - **What it does:** Prevents wireless clients on the same network from communicating directly with each other.
  - **Why:** Makes the wireless network act more like a switch (isolating clients) than a hub (broadcasting to all), enhancing security.
- **3. Choose the Strongest Security Protocol:**
  - **Recommendation:** Always use the highest level of security your devices support.
  - **Order of preference:** **WPA3 > WPA2 > WPA > WEP**.
  - **Never use WEP or WPA** as they are outdated and easily cracked.
  - **WPA2 with AES** is a strong, widely used standard.
- **4. Use a Strong Pre-Shared Key (PSK):**
  - **Recommendation:** Use a long (8-63 characters) and complex passphrase.
  - **Why:** A strong passphrase makes it much harder for attackers to guess or brute-force their way into your network.
- **5. Configure MAC Filtering:**
  - **What it does:** Creates an access list that only allows devices with specific MAC addresses to connect to the network.
  - **Why (Exam Perspective):** Considered a layer of security.
  - **Real-World Limitation:** Provides minimal security as MAC addresses can be easily spoofed (cloned) by a determined attacker in seconds. Can be a management headache.
- **6. Disable WPS (Wi-Fi Protected Setup):**
  - **What it is:** A feature (often a push-button) designed to simplify connecting devices using an 8-digit PIN.
  - **Why disable it:** **Highly insecure.** A design flaw makes the PIN vulnerable to brute-force attacks, which can be completed in minutes.
- **7. Disable Remote Management:**
  - **What it does:** Prevents the router's web-based configuration interface from being accessible from the internet.
  - **Why:** A critical security measure. If enabled, it exposes your router's login page to the entire internet, making it a target for attackers. It should be disabled by default.