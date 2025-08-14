## 💡 When Wireless Security Fails (OBJ 2.3)

This lesson demonstrates the insecurity of the WEP (Wired Equivalent Privacy) protocol by cracking its pre-shared key. **Disclaimer:** This demonstration is for educational purposes only. Attacking a network without permission is illegal. WEP is **fundamentally broken** and provides no real security. An attacker with a modern laptop and open-source tools can crack a WEP key in a matter of minutes. **Never use WEP.** Always upgrade to WPA2 or, preferably, WPA3.

✅ **Key Vulnerability**
- WEP's use of a short, 24-bit Initialization Vector (IV) that is sent in plain text, allowing attackers to capture enough of them to reverse-engineer the encryption key.

✅ **Tools Used (Aircrack-ng Suite)**
- **`airodump-ng`:** For scanning wireless networks and capturing packets.
- **`aireplay-ng`:** For injecting packets (e.g., fake authentication, ARP replays).
- **`aircrack-ng`:** For cracking the WEP key from the captured data.

✅ **The WEP Cracking Process (Simplified Steps)**
- **1. Scan for Networks:**
  - Use `airodump-ng` to scan for nearby wireless networks and identify the target WEP-protected network, its BSSID (MAC address), and channel.
- **2. Capture IVs:**
  - Use `airodump-ng` again, but this time focused on the target's BSSID and channel, to capture the initialization vectors (IVs) and save them to a file.
- **3. Fake Authentication:**
  - Use `aireplay-ng` to perform a "fake authentication" with the access point. This associates the attacker's MAC address with the network, a prerequisite for the next step.
- **4. ARP Request Replay Attack:**
  - Use `aireplay-ng` to inject ARP request replay packets into the network. This stimulates the access point to generate a large number of new packets with new IVs, speeding up the data collection process.
- **5. Crack the Key:**
  - Use `aircrack-ng` and point it to the capture file containing the IVs.
  - The tool analyzes the captured IVs and, once enough have been collected (typically 10,000-25,000), it can mathematically determine the WEP key.
- **6. Connect to the Network:**
  - Use the cracked WEP key to connect to the wireless network and gain access.