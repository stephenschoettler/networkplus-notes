## 💡 Domain Name System (DNS) Attacks (OBJ 4.2)

DNS's purpose is to translate human-friendly domain names into IP addresses that computers understand. Its critical role makes it a prime target for cyberattacks.

✅ **Types of DNS Attacks**
- **1. DNS Cache Poisoning (DNS Spoofing):**
  - **Mechanism:** Corrupting the DNS cache data of a DNS resolver with false information, directing traffic to an attacker-controlled (malicious) website.
  - **Mitigation:** DNSSEC, secure network configurations, firewalls.
- **2. DNS Amplification Attack:**
  - **Mechanism:** Exploits DNS resolution to overwhelm a target system. Attacker sends small query with spoofed victim IP to open DNS server, which sends large response back to victim (DoS).
  - **Mitigation:** Set size limits on DNS responses, rate limit DNS response traffic.
- **3. DNS Tunneling:**
  - **Mechanism:** Encapsulates non-DNS traffic within DNS queries/responses over port 53 to bypass firewall rules.
  - **Purpose:** Command and control, data exfiltration.
  - **Mitigation:** Regularly monitor and analyze DNS logs for unusual patterns.
- **4. Domain Hijacking (Domain Theft):**
  - **Mechanism:** Changing the registration of a domain name without the original registrant's permission.
  - **Impact:** Loss of control over website, redirection to malicious site.
  - **Mitigation:** Regular updates, secure account info, use domain registry lock services.
- **5. DNS Zone Transfer Attack:**
  - **Mechanism:** Attacker tries to get a copy of the entire DNS zone data by pretending to be an authorized system.
  - **Impact:** Exposes sensitive network infrastructure info, used for reconnaissance.
  - **Mitigation:** Restrict zone transfers to authorized secondary DNS servers only.