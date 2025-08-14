## 💡 Subnetting by Hand (OBJ 1.7)

This section covers a quick, mental shortcut to solve subnetting problems without complex calculations, especially useful for the Network+ exam. Memorize the sequence: `1, 2, 4, 8, 16, 32, 64, 128, 256`. This sequence helps determine both the number of subnets and the number of IPs per subnet. This method becomes very fast with practice. Re-watch the video or practice problems until it "clicks."

✅ **Using the "Magic Numbers" for CIDR (`/24` to `/32`)**
- **To find the Number of Subnets:**
  - Start counting from `/24` as 1 subnet. Each increment in CIDR doubles the number of subnets.
  - `/24` = 1 subnet
  - `/25` = 2 subnets
  - `/26` = 4 subnets
  - `/27` = 8 subnets
  - `/28` = 16 subnets
  - `/29` = 32 subnets
  - `/30` = 64 subnets
  - `/31` = 128 subnets (non-standard, Cisco point-to-point)
  - `/32` = 256 subnets (single host)
- **To find the Number of IPs per Subnet (Block Size):**
  - Start from `/24` as 256 IPs. Each increment in CIDR halves the number of IPs.
  - `/24` = 256 IPs
  - `/25` = 128 IPs
  - `/26` = 64 IPs
  - `/27` = 32 IPs
  - `/28` = 16 IPs
  - `/29` = 8 IPs
  - `/30` = 4 IPs (2 usable)
  - `/31` = 2 IPs (0 usable, for point-to-point links)
  - `/32` = 1 IP (1 usable, for a single host)

✅ **Finding Network ID, First Host, Last Host, and Broadcast ID**
- This is the most common application of subnetting on the exam.
- **Steps:**
  - 1. **Determine Block Size:** Use the "magic numbers" to find the total number of IPs in the subnet for the given CIDR.
  - 2. **Identify Network IDs:** These are multiples of the block size. Find the multiple that the given IP address falls into.
  - 3. **Network ID:** The multiple of the block size that is less than or equal to the given IP's last octet.
  - 4. **Broadcast ID:** The Network ID of the *next* subnet, minus 1.
  - 5. **First Host:** Network ID + 1.
  - 6. **Last Host:** Broadcast ID - 1.
- **Example 1: `171.129.67.160/25`**
  - `/25` means a block size of 128 IPs.
  - Multiples of 128: `0, 128, 256...`
  - The IP `160` falls into the `128` block.
  - **Network ID:** `171.129.67.128`
  - **First Host:** `171.129.67.129`
  - **Broadcast ID:** `171.129.67.255` (since the next block would start at `256`)
  - **Last Host:** `171.129.67.254`
- **Example 2: `56.187.210.21/28`**
  - `/28` means a block size of 16 IPs.
  - Multiples of 16: `0, 16, 32, 48...`
  - The IP `21` falls into the `16` block.
  - **Network ID:** `56.187.210.16`
  - **First Host:** `56.187.210.17`
  - **Broadcast ID:** `56.187.210.31` (since the next block would start at `32`)
  - **Last Host:** `56.187.210.30`