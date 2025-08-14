## 💡 Subnetting (OBJ 1.7)

Subnetting is the process of taking a large IP network and logically dividing it into smaller, more manageable subnetworks.
**Subnetting Exam Tip (Memorize this Chart for /24 and higher):**
| CIDR Notation | Borrowed Bits (s) | Number of Subnets (2^s) | Host Bits (h) | Total IPs (2^h) | Usable IPs (2^h - 2) |
| :------------ | :---------------- | :---------------------- | :------------ | :-------------- | :------------------- |
| `/24`         | 0                 | 1                       | 8             | 256             | 254                  |
| `/25`         | 1                 | 2                       | 7             | 128             | 126                  |
| `/26`         | 2                 | 4                       | 6             | 64              | 62                   |
| `/27`         | 3                 | 8                       | 5             | 32              | 30                   |
| `/28`         | 4                 | 16                      | 4             | 16              | 14                   |
| `/29`         | 5                 | 32                      | 3             | 8               | 6                    |
| `/30`         | 6                 | 64                      | 2             | 4               | 2                    |
- **Pattern:** As the CIDR notation increases by 1, the number of subnets doubles, and the total/usable IPs per subnet are halved.
- **Common Exam Range:** Most Network+ subnetting questions will involve `/24` to `/30`.

✅ **Purpose/Benefits**
- **Efficient IP Address Utilization:** Prevents wasting large blocks of IP addresses, especially crucial for public IPs.
- **Improved Security:** Creates network segmentation, isolating traffic and limiting the impact of security breaches.
- **Better Bandwidth Control:** Reduces broadcast traffic within segments, improving overall network performance.
- **Facilitates VLANs:** Subnetting is fundamental to implementing Virtual Local Area Networks (VLANs).

✅ **Classful vs. Classless Subnets**
- **Classful Networks:** Use default subnet masks (e.g., `/8` for Class A, `/16` for Class B, `/24` for Class C). These masks align perfectly with octet boundaries (all 1s or all 0s in an octet).
- **Classless Subnets:** Use custom subnet masks (e.g., `/25`, `/26`, `/27`). These involve "borrowing bits" from the host portion of the IP address to extend the network portion, creating more, smaller networks.

✅ **Key Subnetting Formulas**
- **Number of Subnets:** `2^s`
  - `s` = number of **borrowed bits** from the host portion.
- **Number of Assignable Hosts (per subnet):** `2^h - 2`
  - `h` = number of **remaining host bits**.
- **Why `-2`?** Two IP addresses in every subnet are reserved:
  - **Network ID:** The first IP address in the subnet (represents the network itself).
  - **Broadcast ID:** The last IP address in the subnet (used to send data to all devices in that subnet).
  - Neither can be assigned to a host device.

✅ **CIDR Notation (Classless Inter-Domain Routing)**
- **Shorthand:** A concise way to represent the subnet mask by indicating the number of bits in the network portion (e.g., `192.168.1.0/26`).
- **Route Aggregation:** Allows multiple smaller subnets to be summarized into a single, larger route entry, simplifying routing tables.

✅ **VLSM (Variable-Length Subnet Mask)**
- **Concept:** Allows the use of subnets of different sizes within the same larger network.
- **"Subnetting of Subnets":** You can take a subnet and further divide it into even smaller subnets, optimizing IP address allocation for different needs (e.g., a small subnet for a point-to-point link, a larger one for a user segment).
- **Benefit:** Maximizes IP address efficiency and flexibility.
- **Requirement:** Requires modern routing protocols that support classless routing.

✅ **Calculating Network, Broadcast, and Usable IP Ranges**
- **Example: `192.168.1.0/26`** (from chart: 4 subnets, 64 IPs total per subnet)
- **Subnet 1:**
  - Network ID: `192.168.1.0`
  - Usable IPs: `192.168.1.1` to `192.168.1.62`
  - Broadcast ID: `192.168.1.63`
- **Subnet 2:** (Add 64 to previous Network ID)
  - Network ID: `192.168.1.64`
  - Usable IPs: `192.168.1.65` to `192.168.1.126`
  - Broadcast ID: `192.168.1.127`
- **Subnet 3:** (Add 64 to previous Network ID)
  - Network ID: `192.168.1.128`
  - Usable IPs: `192.168.1.129` to `192.168.1.190`
  - Broadcast ID: `192.168.1.191`
- **Subnet 4:** (Add 64 to previous Network ID)
  - Network ID: `192.168.1.192`
  - Usable IPs: `192.168.1.193` to `192.168.1.254`
  - Broadcast ID: `192.168.1.255`
- **Troubleshooting Tip:** If devices are not communicating and there's no router, check if they are in the same subnet based on their IP and subnet mask.