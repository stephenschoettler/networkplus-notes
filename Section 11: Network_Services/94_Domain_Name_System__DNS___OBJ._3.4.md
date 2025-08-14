## 💡 Domain Name System (DNS) (OBJ 3.4)

- DNS (Domain Name System) is the Internet's Phonebook.
- Its purpose is to translate human-readable **domain names** (e.g., `diontraining.com`) into machine-readable **IP addresses** (e.g., `66.123.45.237`).
- This makes it easier for humans to remember website addresses than numeric IP addresses.
- This translation happens seamlessly in the background for users.
- Most home users rely on their ISP's DNS servers; large organizations may run their own.

✅ **FQDN (Fully Qualified Domain Name)**
- A complete domain name that specifies its exact location in the DNS hierarchy.
- Format: `service.domain.tld` (e.g., `www.diontraining.com`, `ftp.diontraining.com`, `mail.diontraining.com`).

✅ **DNS Hierarchy (Five Levels)**
- **1. Root Level:** The highest level, represented by a single dot (`.`). Root name servers contain the global list of Top-Level Domains.
- **2. Top-Level Domain (TLD):**
  - Directly below the root.
  - Examples: `.com`, `.org`, `.net`, `.edu`, `.gov`, country codes like `.uk`, `.fr`.
- **3. Second-Level Domain:**
  - Directly below the TLD, typically the registered domain name (e.g., `diontraining` in `diontraining.com`).
- **4. Subdomain:**
  - Created by organizations under their second-level domain to organize services (e.g., `www`, `ftp`, `mail`, `support`).
- **5. Host:**
  - The lowest and most detailed level, referring to a specific machine or resource (e.g., the `www` host in `www.diontraining.com`).

✅ **URL (Uniform Resource Locator)**
- Specifies how to access a resource on the internet.
- Includes the protocol (e.g., `http://`, `https://`, `ftp://`) followed by the FQDN and optionally a path.
- Example: `https://www.diontraining.com`

✅ **DNS vs. Hosts File**
- **Hosts File:**
  - A local text file on a computer system that maps hostnames to IP addresses.
  - **Precedence:** The system first checks the hosts file. If an entry is found, it uses that information and bypasses DNS.
  - **Use Cases:**
    - **Local Override:** For testing new website configurations before DNS updates.
    - **Blocking:** Redirecting undesirable websites to non-existent addresses (e.g., `127.0.0.1`) to block access.
    - **Malicious Use:** Can be exploited by attackers to redirect users to fake websites (e.g., phishing).
  - **Limitations:** Not scalable for large networks; manual updates are required.
- **DNS:**
  - A globally distributed, hierarchical system for name resolution.
  - More comprehensive and constantly updated than the hosts file.
  - Used when an entry is not found in the local hosts file.