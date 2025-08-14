## 💡 Client Disassociation Issues (OBJ. 5.4)
This section explains client disassociation in wireless networks, covering both legitimate reasons for disconnection and malicious de-authentication attacks, along with troubleshooting tips.

✅ **Client Disassociation Issues (Wireless Networks)**
- **Definition:** When a wireless client disconnects from a Wireless Access Point (AP).

✅ **Legitimate Reasons for Client Disassociation**
- **Idle Timeout:** Client doesn't send/receive traffic for a set period (e.g., 300 seconds/5 minutes default). AP frees up resources.
- **Session Timeout:** After a longer period (e.g., 1800 seconds), client needs to re-authenticate.
- **Wireless Network Changes:** Administrator changes network settings (e.g., SSID, passphrase), forcing clients to reconnect.
- **Manual Deletion:** Administrator manually removes a client from the network.
- **Authentication Timeouts:** Client fails to complete the authentication/key exchange process within the allotted time.
- **Access Point Radio Resets:** AP reboots or its radio is reset, causing all connected clients to disassociate.

✅ **Malicious Disassociation (De-authentication Attack)**
- **Definition:** A common wireless attack where a hacker intentionally forces wireless clients to disassociate from an AP.
- **Purpose:** To capture the authentication handshake packets (e.g., 4-way handshake) when the client attempts to reconnect. These captured packets can then be used to crack the network's pre-shared key/passphrase.

✅ **Troubleshooting Disassociation Issues**
- If a client is continually being de-authenticated, check wireless gateway and wireless controller logs.
- Determine if the disassociation is due to a legitimate reason (listed above) or a potential de-authentication attack.
- Investigate further if the cause is not one of the normal, expected reasons.