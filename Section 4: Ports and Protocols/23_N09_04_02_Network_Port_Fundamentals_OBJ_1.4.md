## 💡 Network Port Fundamentals (OBJ 1.4)

A **port** is a logical opening in a computer that represents a service or application listening for traffic. An IP address is like a street address (the building), and the port is like a room number (the specific service/application within the building). Understand the three port ranges and their characteristics. Remember that clients use ephemeral ports for outgoing connections to well-known or registered ports on servers.

✅ **Port Categories**
- All ports are numbered from 0 to 65,535.
- **1. Well-known Ports:**
  - Numbered from **0 to 1,023**.
  - Reserved for common services (e.g., FTP 20/21, SMTP 25, HTTP 80, HTTPS 443).
- **2. Registered Ports:**
  - Numbered from **1,024 to 49,151**.
  - Registered with IANA (Internet Assigned Numbers Authority) for specific applications.
- **3. Ephemeral Ports (Dynamic/Private Ports):**
  - Numbered from **49,152 to 65,535**.
  - Short-lived, temporary ports chosen randomly by a client for outgoing communication.
  - Can be used by any system without registration.

✅ **Communication Flow (Client to Server)**
- Client sends data from its IP address and a randomly chosen **ephemeral port** to the server's IP address and its **well-known port** (e.g., Port 80 for HTTP).
- Server responds from its IP address and well-known port back to the client's IP address and the ephemeral port.
- The ephemeral port closes after the communication session ends.