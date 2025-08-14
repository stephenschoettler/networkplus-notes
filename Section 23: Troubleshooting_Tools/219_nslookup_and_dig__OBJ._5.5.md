## 💡 nslookup and dig (OBJ. 5.5)
This section introduces `nslookup` and `dig`, command-line tools for querying DNS, along with the `hostname` command, detailing their usage for network troubleshooting and information gathering.

✅ **nslookup and dig**
- Tools for querying DNS (Domain Name System) for troubleshooting and information gathering.

✅ **`nslookup` (Name Server Lookup)**
- Purpose: Queries DNS for domain name to IP mappings or other DNS records.
- Availability: Windows, Linux, Unix, OS X.
- **Non-interactive Mode:**
  - `nslookup [domain_name]` (e.g., `nslookup www.example.com`)
  - Directly returns IP address(es).
- **Interactive Mode:**
  - Type `nslookup` to enter shell.
  - `server [DNS_server_IP/name]`: Change DNS server for queries.
  - `set q=[record_type]` (or `set type=[record_type]` on Linux/Unix/OS X): Specify record type (e.g., `mx`, `cname`, `a`, `aaaa`, `ns`, `soa`).
  - Then enter domain name to query.
  - Useful for detailed DNS troubleshooting and reconnaissance.

✅ **`dig` (Domain Information Groper)**
- Purpose: Another tool for querying DNS name servers.
- Availability: Default on Linux, Unix, OS X; Windows versions available.
- **Usage:**
  - `dig [domain_name]` (e.g., `dig example.com`) - Shows A records by default.
  - `dig -t [record_type] [domain_name]` (e.g., `dig -t mx example.com`) - Specify record type.
- Does NOT have an interactive mode.

✅ **`hostname`**
- Purpose: Displays the hostname of the local system.
- Availability: Windows, Linux, Unix, OS X.
- Usage: Simply type `hostname` at the command prompt.
- Output: Returns the local machine's hostname (e.g., `mycomputer`, `server1.localdomain`).