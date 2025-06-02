
---

# 📅 Day 4 – Log Analysis Basics: Network-Based Attacks on Linux

## 🔍 What I Did

* Booted into my **Ubuntu** machine on WSL with **UFW (Uncomplicated Firewall)** enabled.
* Simulated network activity by initiating outbound traffic from the source IP `172.27.128.1` targeting the destination IP `172.27.132.68` over common service ports like **80 (HTTP)** and **443 (HTTPS)**.
* Used the command:

  ```bash
  sudo dmesg | grep -i 'ufw'
  ```

  to extract UFW logs directly from kernel messages.
* Observed multiple UFW log entries with **\[UFW BLOCK]** messages indicating denied TCP SYN packets.
* These entries had:

  * Protocol: TCP
  * Source Port: various (e.g., 51186, 51187, 51188, 51189)
  * Destination Port: 80, 443
  * Flags: `SYN` only
* Took a screenshot of the terminal output to document the blocked traffic patterns.

## 🧠 What I Learned

* **UFW (Uncomplicated Firewall)** logs kernel-level blocking of unauthorized traffic.
* Detected signs of a **vertical port scan**, where a single IP probes multiple ports on a target system.
* Understood how to analyze fields in a UFW log:

  * `SRC` and `DST` show attacker and target IPs.
  * `SPT` and `DPT` show source and destination ports.
  * `PROTO` indicates the protocol (TCP in this case).
  * Presence of `SYN` flag without `ACK` suggests connection attempts.
* Learned that `dmesg` can be a quick way to analyze live firewall logs without checking log files directly.
* These types of logs help detect **early reconnaissance** efforts like **port scanning**.

## 📸 Screenshots

Screenshots from this lab can be found in the [screenshots](./screenshots) folder.

---

✅ Challenge Repo: [30 Days SOC Challenge](https://github.com/0xrajneesh/30-Days-SOC-Challenge-Beginner)
✍️ Author: [Daniel Orji](https://www.linkedin.com/in/danielorji1542002)

---

