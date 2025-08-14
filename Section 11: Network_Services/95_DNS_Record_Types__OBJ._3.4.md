## 💡 DNS Record Types (OBJ 3.4)

DNS servers store various record types, each serving a specific purpose in name resolution and other services.

✅ **Common DNS Record Types**
- **1. A Record (Address Record):**
  - **Purpose:** Links a **hostname** (e.g., `www.example.com`) to an **IPv4 address**.
  - Example: `www.diontraining.com` -> `45.79.184.180`
  - An `@` symbol often indicates the root domain (e.g., `diontraining.com`).
- **2. AAAA Record (Quad-A Record):**
  - **Purpose:** Links a **hostname** to an **IPv6 address**.
  - Example: `www.diontraining.com` -> `2400:cb00:2049:1::a29f:1804`
- **3. CNAME Record (Canonical Name Record):**
  - **Purpose:** Points a domain name or subdomain to **another domain name** (not directly to an IP address).
  - Used for aliases or redirecting multiple domain names to a single canonical name.
  - Example: `support.diontraining.com` -> `fdus-143-d15.freshdesk.com`
- **4. MX Record (Mail Exchange Record):**
  - **Purpose:** Directs email to a mail server.
  - Indicates how email messages should be routed using SMTP (port 25).
  - **Cannot point to an IP address; must point to a domain name.**
  - Includes a **priority value** (lower number = higher priority) to determine which mail server to try first. Same priority values enable load balancing.
- **5. SOA Record (Start of Authority Record):**
  - **Purpose:** Stores important administrative information about a domain or zone.
  - Includes: domain administrator's email, serial number (versioning), refresh intervals, retry intervals, expire limits, and minimum TTL.
  - Crucial for **zone transfers** (replicating DNS data from a primary to a secondary nameserver). Zone transfers typically use TCP.
- **6. PTR Record (Pointer Record):**
  - **Purpose:** Correlates an **IP address** with a **domain name**. It's the **opposite of an A record**.
  - Used for **Reverse DNS Lookups** (finding a hostname from an IP address).
  - Often stored under the `.arpa` top-level domain (e.g., `33.44.55.66.in-addr.arpa` for `66.55.44.33`).
  - Useful for email deliverability (spam prevention) and logging.
- **7. TXT Record (Text Record):**
  - **Purpose:** Stores arbitrary text data within DNS.
  - Originally for human-readable notes, now widely used for machine-readable data.
  - Common uses: **Domain ownership verification** (e.g., for cloud services) and **email spam prevention** (e.g., SPF, DKIM records).
- **8. NS Record (Nameserver Record):**
  - **Purpose:** Indicates which DNS nameserver is **authoritative** for a domain.
  - Essential for the hierarchical nature of DNS, telling other DNS servers where to find the definitive records for a domain.

✅ **DNS Lookup Types**
- **Forward Lookup:** Resolving a domain name to an IP address (e.g., `www.google.com` -> `172.217.160.142`).
- **Reverse Lookup:** Resolving an IP address to a domain name (uses PTR records).

✅ **Time To Live (TTL)**
- A value associated with each DNS record that tells a DNS resolver (or client's local cache) how long to **cache** a query's answer before requesting a new one.
- Default is often 86,400 seconds (24 hours). Lower TTLs mean faster propagation of DNS changes but more frequent lookups.

✅ **DNS Query Types**
- **Recursive Lookup:** A DNS resolver (e.g., your ISP's DNS server) is asked to provide the complete answer. If it doesn't know, it will query other DNS servers on your behalf until it finds the answer.
- **Iterative Lookup:** A DNS resolver is asked to provide the best answer it has. If it doesn't know the full answer, it will refer the querying client to another DNS server that might know more, and the client then queries that server directly.