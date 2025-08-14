## 💡 Using Cloud Computing (OBJ 1.3)

This lesson provides a practical guide to using cloud computing with Amazon Lightsail, an easy-to-use cloud platform from Amazon Web Services (AWS) that bundles compute, storage, and networking into simple, affordable plans, ideal for beginners.
**Key Benefits Demonstrated:**
- **Elasticity:** Easily scale resources up (vertical scaling by changing plans) or down.
- **Metered Utilization:** Pay only for the resources consumed.
- **Accessibility:** Remote access from anywhere.
- **Flexibility:** Choose OS, applications, and customize as needed.

✅ **Creating a Virtual Server (Instance) in Lightsail**
- **1. Account Setup:** Create an AWS account and access the Lightsail dashboard.
- **2. Instance Creation:** Click "Create instance."
- **3. Region & Availability Zone:** Choose the geographical location closest to you for lower latency.
- **4. Platform & Blueprint:**
  - **Platform:** Select Linux/Unix (cheaper, open-source) or Windows (more expensive due to licensing).
  - **Blueprint:**
    - **OS Only (IaaS):** Choose a specific Linux distribution (e.g., CentOS, Ubuntu) or Windows Server.
    - **App + OS (PaaS):** Includes an operating system plus a pre-installed application (e.g., WordPress, Joomla, Node.js).
- **5. Plan Selection:** Choose a plan based on desired resources (RAM, vCPUs, SSD storage, data transfer) and associated monthly cost. Plans are metered, and often initial months are free.
- **6. Instance Name:** Assign a unique name to your server.
- **7. Create Instance:** Lightsail provisions the hardware, installs the OS, and assigns public/private IP addresses.

✅ **Connecting to Your Instance (SSH)**
- Lightsail provides a convenient browser-based SSH client for remote command-line access.
- You can also connect using your own SSH client.

✅ **Basic Linux Commands Demonstrated (via SSH)**
- `pwd`: Print Working Directory (shows current directory).
- `ls`: List contents of a directory (`ls -la` for long listing with all files, including hidden).
- `touch [filename]`: Creates an empty file.
- `vi [filename]`: Opens the VI text editor.
- `i`: Enter insert mode (to type).
- `Esc`: Exit insert mode.
- `:wq`: Write (save) and Quit.
- `cat [filename]`: Displays the content of a file.

✅ **Managing Your Cloud Instance**
- **Storage Disks:**
  - Instances come with a system disk. Additional SSD-based storage disks can be attached and detached.
  - Storage is billed per GB per month.
  - Detached disks retain data, allowing for data transfer between instances.
- **Metrics:**
  - Monitor instance performance (CPU utilization, burst capacity, network traffic).
  - **Burstable Zone:** Cloud instances often have a "burstable" capacity, allowing temporary spikes in CPU usage beyond the baseline.
- **Snapshots (Backups):**
  - Create point-in-time images of your server's disk.
  - Can be manual or automatic (e.g., daily, retaining 7 most recent).
  - Used for disaster recovery or creating new instances from a known state.
- **Instance Actions:**
  - **Stop:** Powers down the instance (useful for temporary pauses, may still incur storage costs).
  - **Reboot:** Restarts the instance (for applying updates or troubleshooting).
  - **Delete:** Permanently removes the instance and its associated resources.