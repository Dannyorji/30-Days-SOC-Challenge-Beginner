# 📅 Day 6 – Introduction to Wireshark
## 🔍 What I Did
* Launched Wireshark and explored the interface, focusing on the capture panel and display filters.

* Practiced capturing live traffic on my network interface (Wi-Fi) by starting and stopping packet captures.

* Learned how to create and switch between custom profiles to suit specific analysis needs (e.g., malware analysis, general monitoring).

* Used display filters such as:
```  
http
ip.addr == <my-ip-address>
tcp.port == 443
```
to isolate specific protocols and sessions.

* Reviewed captured packets, examined protocol layers (Ethernet, IP, TCP, HTTP), and practiced identifying request/response pairs.

* Tested common filters to trace things like:

  * Source and destination IPs

  * TCP handshakes

  * DNS lookups

  * HTTP GET/POST requests

## 🧠 What I Learned
* Wireshark is a powerful packet analysis tool that allows SOC analysts to inspect and troubleshoot network traffic.

* Creating profiles in Wireshark helps in customizing layouts, coloring rules, and filters for specific investigation types.

* Understanding how to capture and interpret traffic is essential in detecting suspicious activities such as unauthorized access, C2 communications, and data exfiltration.

* Display filters are essential in reducing noise and focusing on indicators of compromise (IOCs).

* Packet-level visibility helps SOC analysts and incident responders verify alerts and understand what’s happening on the wire.

## 📸 Screenshots

Screenshots from this lab can be found in the [screenshots](./screenshots) folder.

---

✅ Challenge Repo: [30 Days SOC Challenge](https://github.com/0xrajneesh/30-Days-SOC-Challenge-Beginner)
✍️ Author: [Daniel Orji](https://www.linkedin.com/in/danielorji1542002)

---
