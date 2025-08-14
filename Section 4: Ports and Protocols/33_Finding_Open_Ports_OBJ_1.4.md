## 💡 Finding Open Ports (OBJ 1.4)

This section covers tools used to find open ports on a network. For the Network+ exam, you need to know *what* a tool like Nmap is used for (e.g., network mapping, finding open ports), not its specific command syntax.

✅ **Nmap (Network Mapper)**
- A popular command-line tool used to scan remote systems (servers) to find open ports and services.
- Can perform ping sweeps, identify open ports, and even determine the operating system of a remote server.
- Used by network technicians for troubleshooting and by security professionals for vulnerability assessment.
- Command example: `nmap -sS -O [IP_Address]` (where `-sS` is SYN scan, `-O` is OS detection).
- Output shows open ports, their state (open), protocol (TCP/UDP), and service name.
- **Security Concern:** Minimizing open ports is crucial for security; each open port represents a potential attack vector. For example, Telnet (port 23) is insecure and should be disabled.

✅ **Zenmap**
- A graphical user interface (GUI) for Nmap, making it easier to use.
- Provides a user-friendly interface to input targets and select scan profiles.
- Displays scan results in a graphical format, including port details, service versions, and host details (OS).
- Knowing service versions (e.g., VSFTP 2.3.4) is critical for security professionals to identify known vulnerabilities.

✅ **scanme.nmap.org**
- A server set up by Nmap for users to practice scanning and learn how to use the tools.