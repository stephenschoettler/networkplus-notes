## 💡 Content Filtering (OBJ 1.2 & 4.3)

Content Filtering is the process of restricting access to certain content, websites, or applications based on specific criteria. Its purpose is to prevent exposure to inappropriate/harmful content, conserve network bandwidth, and comply with legal or organizational policies.

✅ **Methods of Content Filtering**
- **1. URL Filtering:** Blocks access to specific websites based on their Uniform Resource Locator (URL).
- **2. Keyword Filtering:** Scans webpages for specific keywords/phrases and blocks the page if detected.
- **3. Protocol and Port Filtering:** Blocks certain types of network traffic based on the protocol or port used.

✅ **Proxy Servers (Common Implementation Tool)**
- **Definition:** A server that acts as an intermediary between a user's device and the internet.
- **Types of Proxies:**
  - **1. Web Proxy:** Retrieves webpages. Can be used to bypass content filters (a concern for organizations).
  - **2. Reverse Proxy:** Manages incoming internet traffic to an organization. Uses: Load balancing, improving security (filtering malicious traffic), caching.
  - **3. Transparent Proxy:** Monitors and filters internet traffic without the user's knowledge. Uses: Blocking access, logging user activity, enforcing policies.
- **Benefits of Proxy Servers (General):**
  - Improved security (filter malicious traffic, prevent unauthorized access).
  - Anonymity (hide user's IP address).
  - Content filtering (block specific sites/content).
  - Performance improvement (cache frequently accessed resources).