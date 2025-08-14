## 💡 netstat (Network Statistics) (OBJ. 5.5)
This section introduces `netstat`, a command-line tool for displaying network connections, routing tables, and interface statistics, detailing its basic output and various options for network troubleshooting and analysis.

✅ **netstat (Network Statistics)**
- Purpose: Displays information for IP-based connections on a client.
- Includes: Current sessions, source/destination IPs, port numbers.
- Availability: Windows, Linux, UNIX, OS X.

✅ **Basic `netstat` Output**
- Columns: `Protocol`, `Local Address`, `Foreign Address`, `State`.
- `Local Address`: Your IP:Port.
- `Foreign Address`: Destination IP:Port (resolves to hostname/service if known).
- `State`: TCP connection state (e.g., `ESTABLISHED`, `TIME_WAIT`, `LISTENING`).

✅ **`netstat` Options**
- `-a`: **All connections.** Shows all sockets (listening and non-listening) and all protocols (TCP, UDP, ICMP).
- `-n`: **Numeric addresses.** Displays IPs and port numbers numerically (no hostname/service resolution).
- `-an` (or `-na`): Combines `-a` and `-n`.
- `-o`: **Owner (PID).** (Windows-specific, but concept applies). Adds a `PID` (Process Identification Number) column.
  - Use with `tasklist` (Windows) or `ps` (Linux/macOS) to identify the application/service creating the connection.
  - Example: `netstat -ano` (very useful for malware investigation).
- `-s`: **Statistics.** Displays network statistics per protocol (IPv4, IPv6, ICMP, TCP, UDP).
  - Shows packets delivered, discarded, errors, etc.
  - Use for network health assessment and establishing performance baselines.