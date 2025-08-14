## 💡 DNS and NTP Issues (OBJ. 5.3)
This section covers common troubleshooting scenarios for Domain Name System (DNS) and Network Time Protocol (NTP) services, which are crucial for network functionality and time synchronization.

✅ **DNS (Domain Name System) Issues**
- Purpose: Matches domain names to IP addresses.
- **Troubleshooting Scope:**
  - **Single Client Issue:** Likely client-side TCP/IP settings.
    - Verify assigned DNS server IP (`ipconfig`, `ifconfig`, `ip` commands).
    - Check connectivity to DNS server (ping).
    - If reachable: Flush DNS cache (`ipconfig /flushdns`), or change to a different DNS server (e.g., Google's 8.8.8.8).
  - **Network-Wide Issue:** Likely DNS server problem.
  - **A Records:** Ensure domain name and IP address are correctly entered (no typos).
  - **CNAME Records:** Ensure source and destination domain names are spelled correctly.
  - Verify records using `nslookup` command.
  - **TTL (Time To Live):** Incorrectly set TTL can cause caching issues.
    - High TTL: Old DNS records remain cached for too long.
    - Low TTL (e.g., 300 seconds/5 minutes): Reduces caching issues for frequent changes.
  - **DNS Latency:** High latency if DNS servers are far from users.
  - Reduce by using DNS servers closer to users (local, ISP-hosted).

✅ **NTP (Network Time Protocol) Issues**
- Purpose: Synchronizes system clocks across devices, critical for distributed applications (e.g., network authentication).
- **Common NTP Issues & Troubleshooting:**
  - **1. NTP packets not being received:**
    - Indicates general network communication issue (Layer 1, 2, or 3).
    - Verify physical connectivity, MAC address communication (LAN), or IP address communication (WAN).
    - Could be a DNS issue if NTP server is referred to by domain name.
  - **2. NTP packets received but not processed:**
    - Ensure NTP service/process is running and configured to read/process packets on the client/server.
    - Lack of processing leads to time synchronization issues affecting other services (HTTPS, authentication).
  - **3. NTP packets processed but with errors/packet loss:**
    - Leads to loss of time synchronization.
    - High "dispersion" or "delay" values indicate packets are taking too long to reach the client from the server, making the timestamp unreliable.
    - Caused by saturated links or buffering.
    - Ensure adequate network connectivity and no saturation to allow timely NTP packet delivery.