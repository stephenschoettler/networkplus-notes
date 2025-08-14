## 💡 Subnetting Practice (OBJ 1.7)

This section provides practice problems for applying subnetting concepts. Memorize the subnetting chart (CIDR, total IPs, usable IPs) and write it down as a "brain dump" at the start of your exam. This will save significant time. Practice subnetting problems, especially those in the Class C range (`/24` to `/30`), as these are common on the Network+ exam. Understanding the underlying formulas (`2^s` and `2^h - 2`) reinforces the chart's logic.

✅ **Practice Problem 1: Variable-Length Subnet Masking (VLSM) Scenario**
- **Scenario:** Given a `10.10.10.0/24` network (256 total IPs), assign minimum-sized subnets for departments with varying user counts.
- **Key Rule:** When determining the required subnet size, always add 2 to the number of required hosts to account for the **Network ID** and **Broadcast ID**. Then, find the smallest power of 2 that accommodates this total.
- **Example: IT Department (54 users)**
  - Required IPs: 54 (users) + 2 (Network/Broadcast) = 56 IPs.
  - Smallest power of 2 that fits 56 is 64.
  - From the chart, 64 total IPs corresponds to a `/26` subnet (62 usable IPs).
- **Example: Instructors (32 users)**
  - Required IPs: 32 (users) + 2 (Network/Broadcast) = 34 IPs.
  - Smallest power of 2 that fits 34 is 64.
  - This also requires a `/26` subnet.
- **Example: Sales (5 users)**
  - Required IPs: 5 (users) + 2 (Network/Broadcast) = 7 IPs.
  - Smallest power of 2 that fits 7 is 8.
  - From the chart, 8 total IPs corresponds to a `/29` subnet (6 usable IPs).
- **Calculating Unused Portion:**
  - Sum all allocated total IPs (e.g., 64 + 64 + 8 + 8 = 144).
  - Subtract from the original total IPs (e.g., 256 - 144 = 112 remaining).
  - Round *down* the remaining IPs to the nearest power of 2 to find the largest possible unused block (e.g., 112 rounds down to 64, which is a `/26`).

✅ **Practice Problem 2: Counting Assignable IP Addresses**
- **Question:** How many assignable IP addresses exist in the network `172.16.1.0/27`?
- **Key Insight:** The IP address (`172.16.1.0`) is irrelevant for this type of question; only the CIDR notation (`/27`) matters.
- **Solution:**
  - 1. Look up `/27` on your chart: It corresponds to 32 total IPs.
  - 2. The question asks for "assignable" IPs, meaning you must subtract the Network ID and Broadcast ID.
  - 3. `32 - 2 = 30` assignable IPs.
- **Important Distinction:**
  - "Total IPs" = `2^h` (includes Network and Broadcast IDs).
  - "Assignable IPs" or "Usable IPs" = `2^h - 2` (excludes Network and Broadcast IDs).
  - Pay close attention to the wording in exam questions!

✅ **Practice Problem 3: Another Assignable IPs Example**
- **Question:** How many assignable IPs exist in the network `192.168.1.0/28`?
- **Solution:**
  - 1. Look up `/28` on your chart: It corresponds to 16 total IPs.
  - 2. Subtract 2 for assignable: `16 - 2 = 14` assignable IPs.