## 💡 Address Translation (OBJ 2.1)

- Address Translation (NAT/PAT) was developed to help conserve the limited number of IPv4 addresses.
- It allows multiple private IP addresses to share a smaller number of public IP addresses.
- Private IP addresses are not routable on the public internet.
- **Memory Aid:** "Global" means public, "Local" means private.

✅ **Network Address Translation (NAT)**
- Translates private IP addresses to public IP addresses for routing over public networks (like the internet).
- **Types of NAT:**
  - **1. Dynamic NAT (DNAT):**
    - Automatically assigns a public IP address from a pool of available public IPs to a private IP address on a one-to-one basis.
    - When a device needs internet access, it "borrows" a public IP from the pool. When done, the IP is returned to the pool.
    - Useful for maximizing public IP space for internal clients when not all clients need simultaneous internet access.
  - **2. Static NAT (SNAT):**
    - Manually assigns a specific private IP address to a specific public IP address on a one-to-one, permanent basis.
    - Often used for servers or devices that need to be consistently accessible from the internet (e.g., a web server).
    - Primarily a security feature, hiding the internal IP address.

✅ **Port Address Translation (PAT)**
- The most common form of address translation used today (e.g., in home networks).
- Allows **multiple private IP addresses to share a single public IP address** (many-to-one translation).
- Achieves this by using different **port numbers** to keep track of individual connections from internal devices.
- When a request leaves the network, the router assigns a unique port number to each internal connection. When a response returns, the router uses the port number to direct the traffic to the correct internal device.

✅ **NAT IP Address Terminology (for the Exam)**
- **Inside Local:** The private IP address of an inside device (e.g., your computer's 192.168.1.10).
- **Inside Global:** The public IP address used by an inside device when communicating with the outside world (e.g., your home router's public IP).
- **Outside Local:** The private IP address of an outside device as seen by the inside network (less common, often the private IP of a server on a remote network if it's behind another NAT).
- **Outside Global:** The public IP address of an outside device (e.g., a public web server's IP address).