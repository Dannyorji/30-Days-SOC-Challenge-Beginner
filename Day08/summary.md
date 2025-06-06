# 📅 Day 8 – Network Monitoring: Inspecting IP and TCP Connections
## 🔍 What I Did
* Ran the `ip addr` command on my Linux machine to view detailed network interface information.

* Identified my system's IP address, loopback address, and MAC address from the output.

* Used the `ss -tuln` command to list all active TCP/UDP listening ports, which is helpful for spotting open services.

* Specifically analyzed TCP connections using:
    `ss -t`
* Inspected connection states such as `LISTEN`, `ESTABLISHED`, and `TIME-WAIT` to understand which services are actively communicating.

* Reviewed TCP packet behavior using packet capture showing the SYN flag, which initiates a TCP handshake.

## 🧠 What I Learned
* The `ip addr` command provides essential interface details including private IP, interface name, and MAC address, which help in device identification and tracking in a SOC environment.

* The `ss` command is a modern replacement for `netstat`, useful for quickly auditing active connections or detecting unauthorized services.

* TCP connections begin with a SYN packet, and monitoring these packets is crucial in identifying:

   * Reconnaissance activity (e.g., port scanning)

   * SYN flood attacks (a form of DoS)

* Understanding TCP flags like `SYN`, `ACK`, and their role in the 3-way handshake is fundamental to network traffic analysis and intrusion detection.

* Knowing the difference between connection states helps in correlating log data during incident response.

## 📸 Screenshots

Screenshots from this lab can be found in the [screenshots](./screenshots) folder.
* `ip addr.png`: Displays IP configuration and MAC address

* `tcp ss.png`: Shows TCP connection status

* `tcp syn.png`: Highlights TCP SYN packet in traffic

---

✅ Challenge Repo: [30 Days SOC Challenge](https://github.com/0xrajneesh/30-Days-SOC-Challenge-Beginner)
✍️ Author: [Daniel Orji](https://www.linkedin.com/in/danielorji1542002)

---
