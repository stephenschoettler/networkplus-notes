## 💡 IP Configuration Issues (OBJ. 5.3)
This section addresses common problems arising from incorrect IP configurations on network clients, including issues with default gateways, subnet masks, and DNS server settings.

✅ **IP Configuration Issues**
- Every network client needs four key pieces of information to communicate:
  - 1. IP Address
  - 2. Subnet Mask
  - 3. Default Gateway IP Address
  - 4. DNS Server IP Address

✅ **Common Issues & Troubleshooting**
- **1. Incorrect Default Gateway:**
  - Problem: Client cannot access resources outside its local subnet (e.g., the internet).
  - Cause: The default gateway IP address configured on the client is not on the same logical subnet as the client's IP address (based on its subnet mask).
  - Solution:
    - Change the client's default gateway to an IP address within its current subnet that belongs to the router.
    - Alternatively, change the client's IP address to be on the same subnet as the router's interface.
- **2. Incorrect Subnet Mask:**
  - Problem: Client's IP address and default gateway appear correct but are actually in different subnets due to an incorrect subnet mask. This prevents routing.
  - Cause: Misconfigured subnet mask, leading to the client's IP falling outside the expected range for its configured gateway.
  - Solution:
    - Correct the subnet mask on the client to accurately reflect its network segment.
    - Adjust the client's IP address to be on the same subnet as the router's interface.
- **3. Incorrect DNS Server IP Address:**
  - Problem: Client can ping IP addresses but cannot resolve domain names (e.g., cannot access websites by name).
  - Cause: DNS server IP is incorrect, unreachable, or the DNS server itself is not functioning.
  - Solution:
    - Verify the configured DNS server IP on the client.
    - Ensure the DNS server is reachable and operational.
    - If no local DNS server is available, use public DNS servers (e.g., Google DNS: 8.8.8.8 and 8.8.4.4).