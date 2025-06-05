# 📅 Day 7 – Wireshark Basics: ICMP Protocol Analysis
## 🔍 What I Did
* Opened the provided `Protocol_Analysis_pcap.pcapng` file in Wireshark.

* Applied display filters to isolate ICMP traffic:

   * `icmp.type == 8` ➜ Echo Request

   * `icmp.type == 0` ➜ Echo Reply

* Identified Echo Request packets initiated by one host and the corresponding Echo Reply packets from the other host.

* Analyzed the structure of ICMP packets, noting the following fields:

   * Type (8 for request, 0 for reply)

   * Code

   * Checksum

   * Identifier (BE)

   * Sequence number (BE)

* Matched request and reply pairs by comparing the Identifier and Sequence number.

* Took screenshots of both Echo Request and Echo Reply packets in Wireshark for documentation.

## 🧠 What I Learned
* ICMP is a network-layer protocol used for diagnostics like `ping` and error reporting.

* Echo Requests (type 8) and Echo Replies (type 0) are used to test if a destination is reachable.

* ICMP packets do not use TCP/UDP ports—they operate directly over IP.

* By examining the Identifier and Sequence Number, you can match request and reply packets to confirm successful communication.

* Wireshark's display filters (like `icmp.type == 8`) help focus analysis on specific traffic types efficiently.

* Understanding ICMP traffic is essential for detecting network connectivity issues or even potential ICMP-based attacks (e.g., ping floods).

Screenshots from this lab can be found in the [screenshots](./screenshots) folder.

---

✅ Challenge Repo: [30 Days SOC Challenge](https://github.com/0xrajneesh/30-Days-SOC-Challenge-Beginner)
✍️ Author: [Daniel Orji](https://www.linkedin.com/in/danielorji1542002)

---
