## 💡 Understanding DNS (OBJ 3.4)

This lesson demonstrates the DNS resolution process using a simulated network, showing how a client accesses a website. DNS resolution is a hierarchical process involving multiple servers and ARP lookups at each network segment to translate human-readable domain names into machine-routable IP addresses, enabling access to internet resources.

✅ **Network Setup for DNS Demonstration**
- **Client:** Initiates the request (e.g., `diontraining.com`).
- **Local DNS Server:** First point of contact for the client's DNS queries.
- **Company Router:** Connects the local network to the internet.
- **Internet Router:** Represents the internet backbone.
- **Root DNS Server:** Contains information about Top-Level Domains (TLDs) like `.com`.
- **Authoritative DNS Server:** Holds the definitive DNS records for a specific domain (e.g., `diontraining.com`).
- **Web Server:** Hosts the website content.

✅ **The DNS Resolution Process**
- **1. Client Request:** Client wants to access `diontraining.com`. It first checks its local DNS cache.
- **2. Local DNS Query:** If not in cache, the client sends a DNS query to its configured **Local DNS Server**.
- **3. Local DNS to Root DNS:** If the Local DNS Server doesn't have the record, it queries the **Root DNS Server** (e.g., for `.com`).
  - *Note:* ARP is used at each hop to resolve IP addresses to MAC addresses for local delivery.
- **4. Root DNS to Authoritative DNS:** The Root DNS Server refers the Local DNS Server to the **Authoritative DNS Server** for `diontraining.com`.
- **5. Authoritative DNS Response:** The Authoritative DNS Server provides the IP address for `diontraining.com` (e.g., `10.4.0.3`).
- **6. Response Back to Client:** The IP address is sent back through the chain of DNS servers (Authoritative -> Root -> Local -> Client).

✅ **DNS Caching for Efficiency**
- DNS responses are **cached** at various levels (client, local DNS server, root DNS server).
- **TTL (Time To Live):** Determines how long a record is cached. Once TTL expires, the record is invalidated, and a new lookup is performed.
- Caching significantly speeds up subsequent lookups for the same domain.

✅ **Final HTTP Request and Response**
- Once the client has the IP address for `diontraining.com`, it no longer needs DNS.
- The client then sends an **HTTP GET request** directly to the web server's IP address.
- The web server processes the request and sends the webpage content back to the client.
- This HTTP communication occurs directly between the client and the web server, bypassing DNS servers.