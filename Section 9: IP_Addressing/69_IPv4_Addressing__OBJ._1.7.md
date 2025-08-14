## 💡 IPv4 Addressing (OBJ 1.7)

An IPv4 address is a 32-bit numerical label assigned to each device on a network. Understanding the structure of an IPv4 address (network and host portions determined by the subnet mask) is fundamental to networking. While classful addressing is a historical concept, modern networking relies on classless addressing (subnetting and CIDR) for efficient use of the limited IPv4 address space.

✅ **IPv4 Addressing Fundamentals**
- **Definition:** A 32-bit numerical label assigned to each device on a network.
- **Format:**
  - **Dotted-Decimal Notation:** Written as four decimal numbers separated by dots (e.g., `192.168.1.4`). Easier for humans.
  - **Binary:** Computers see it as a 32-bit binary number (e.g., `11000000.10101000.00000001.00000100`).
  - **Octets:** Each of the four decimal numbers is called an octet, representing 8 bits of the address. Each octet can have a value from 0 to 255.

✅ **Network vs. Host Portions**
- Every IPv4 address is divided into two parts:
  - **1. Network Portion:** Identifies the network the device is on.
  - **2. Host Portion:** Identifies the specific device on that network.
- **Subnet Mask:** A 32-bit number that determines which part of the IP address is the network portion and which is the host portion.
  - In binary, `1`s in the subnet mask correspond to the network portion of the IP address.
  - In binary, `0`s in the subnet mask correspond to the host portion of the IP address.

✅ **IPv4 Address Classes (Classful Addressing)**
- A historical method of categorizing IPv4 addresses. The class is determined by the value of the first octet.
| Class | First Octet Range | Default Subnet Mask | Network/Host Portions |
| :--- | :--- | :--- | :--- |
| **A** | 1-127 | `255.0.0.0` (/8) | N.H.H.H |
| **B** | 128-191 | `255.255.0.0` (/16) | N.N.H.H |
| **C** | 192-223 | `255.255.255.0` (/24) | N.N.N.H |
| **D** | 224-239 | N/A | Reserved for Multicasting |
| **E** | 240-255 | N/A | Reserved for Experimental Use |

✅ **Classful vs. Classless Subnetting**
- **Classful:** Using the default subnet mask for a given address class (e.g., using `255.255.255.0` for a Class C address). This is inflexible and often wasteful.
- **Classless:** Using a custom subnet mask to borrow bits from the host portion to create more network portions. This process is called **subnetting**.
- **CIDR (Classless Inter-Domain Routing) Notation:** A shorthand for writing the subnet mask by indicating the number of network bits with a slash (e.g., `/24` is the same as `255.255.255.0`).