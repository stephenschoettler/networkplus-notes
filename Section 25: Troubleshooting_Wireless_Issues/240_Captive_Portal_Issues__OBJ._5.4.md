## 💡 Captive Portal Issues (OBJ. 5.4)
This section defines captive portals, explains their common implementation methods, and provides troubleshooting steps for issues that prevent proper redirection and network access.

✅ **Captive Portals**
- **Definition:** A webpage displayed to newly connected users of a wireless network before they are granted broader access to network resources.
- **Purpose:** Commonly used for authentication, payment, acceptance of End User License Agreements (EULAs) or Acceptable Use Policies (AUPs), or collecting user information.
- **Common Uses:** Hotels, restaurants, airports, public Wi-Fi.

✅ **Common Implementation Methods (Redirects)**
- **HTTP Redirect:** All HTTP traffic is redirected to a controlled web server, which then redirects the client to the captive portal page (using HTTP status code 302).
- **ICMP Redirect:** (Less common) Uses ICMP messages to redirect traffic.
- **DNS Redirect (Most Common):** When a client attempts to resolve a domain name, the network's DNS server redirects the request to the captive portal page.

✅ **Troubleshooting Captive Portal Issues**
- **Problem:** Captive portal doesn't redirect properly, preventing network access.
- **Troubleshooting Steps (Sequential):**
  - **1. Attempt to browse any common website:** Open a web browser and try to navigate to a well-known site (e.g., `google.com`, `facebook.com`). This often triggers the HTTP or DNS redirect.
  - **2. Directly access the default gateway:** If step 1 fails, determine the wireless network's default gateway IP address and type `http://[default_gateway_IP]` into the web browser. This can force the captive portal page to load.
  - **3. Check DNS settings (for DNS redirect issues):**
    - If your device's DNS server is statically configured (e.g., to a public DNS like 8.8.8.8), it bypasses the network's DNS redirection.
    - **Solution:** Change your device's DNS settings to "obtain DNS automatically" (via DHCP) to ensure it uses the network's assigned DNS server. Then re-attempt step 1.