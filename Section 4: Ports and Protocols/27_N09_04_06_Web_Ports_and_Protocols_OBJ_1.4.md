## 💡 Web Ports and Protocols (OBJ 1.4)

Web Ports and Protocols are standardized rules and numerical gateways for data transmission over the internet for websites. Always prioritize HTTPS (Port 443) for secure web browsing and sensitive data. Understand that HTTP (Port 80) is unencrypted and should be avoided for any sensitive transactions.

✅ **1. HTTP (Hypertext Transfer Protocol)**
- **Purpose:** Foundation of data communication on the World Wide Web. Used for requesting web pages and content.
- **Port:** 80 (TCP).
- **Functionality:** Sends plain text requests from client to server, and receives plain text responses (HTML, images, etc.).
- **Insecure:** Data transferred in **plain text (unencrypted)**, making it vulnerable to eavesdropping and on-path attacks. **Never enter sensitive information** (login credentials, personal data, credit card details) on an HTTP (Port 80) website.

✅ **2. HTTPS (Hypertext Transfer Protocol Secure)**
- **Purpose:** Secure version of HTTP, adding a layer of encryption.
- **Port:** 443 (TCP).
- **Functionality:** Uses SSL (Secure Sockets Layer) or TLS (Transport Layer Security) to encrypt data transferred between client and server.
- **Identification:** Indicated by `https://` in the URL or a padlock icon in the browser.
- **Importance:** Crucial for websites handling sensitive data (online banking, e-commerce, login pages). Many websites automatically redirect HTTP traffic to HTTPS.

✅ **Key Differences between HTTP (Port 80) and HTTPS (Port 443)**
  - **1. Security and Encryption**
  - **2. Default Usage**
  - **3. SEO and Trust**