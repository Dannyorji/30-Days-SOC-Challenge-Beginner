# 📅 Day 10 – Wireshark Basics: TLS Protocol Analysis
## 🔍 What I Did
* Opened a PCAP file in Wireshark containing encrypted TLS traffic.

* Applied specific filters to isolate different aspects of the TLS handshake:

  * `tls` to view all TLS-related packets.

  * `tls.handshake.type == 1` to filter for Client Hello messages, which initiate the TLS handshake.

  * `tls.record.version == 0x0303` to specifically identify TLS 1.2 traffic.

* Analyzed the Client Hello packet to observe:

  * The supported cipher suites

  * The TLS version used

  * The extensions such as Server Name Indication (SNI), which can reveal the hostname the client wants to communicate with.

* Took relevant screenshots of each filtered view and notable packet details.

🧠 What I Learned
* TLS (Transport Layer Security) is critical for securing communication over the internet, and analyzing its handshake can reveal useful metadata even if the traffic is encrypted.

* The Client Hello message is the first step of the TLS handshake and includes key information like:

  * TLS version the client supports

  * Cipher suites it can use

  * Extensions such as SNI (helpful for identifying the domain name requested)

* Using `tls.handshake.type == 1` helps pinpoint the start of new TLS sessions.

* The `tls.record.version == 0x0303` filter identifies sessions that use TLS 1.2, which is still widely supported and used.

* Even though TLS encrypts payloads, metadata in handshake packets remains visible and can be analyzed for threat hunting, protocol validation, or network forensics.

## 📸 Screenshots

Screenshots from this lab can be found in the [screenshots](./screenshots) folder.
* Filtered TLS traffic

* Client Hello packet analysis

* TLS 1.2 version detection

---

✅ Challenge Repo: [30 Days SOC Challenge](https://github.com/0xrajneesh/30-Days-SOC-Challenge-Beginner)
✍️ Author: [Daniel Orji](https://www.linkedin.com/in/danielorji1542002)

---
