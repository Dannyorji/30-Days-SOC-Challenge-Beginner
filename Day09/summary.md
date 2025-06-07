# 📅 Day 9 – Wireshark Basics: HTTP Protocol Analysis
## 🔍 What I Did
* Launched Wireshark and opened a PCAP file containing captured HTTP traffic.

* Applied multiple filters to isolate relevant HTTP traffic:

  * Used the filter `http` to display all HTTP protocol packets.

  * Then filtered further with `http.request.method == "GET"` to narrow down to GET requests.

  * Finally, applied `http.request.uri` to inspect the requested URIs within those GET requests.

*Examined the source and destination IPs, host headers, and full URI paths requested by the client.

*Captured relevant screenshots to document my filtering and findings.

## 🧠 What I Learned
* Wireshark is an essential tool for network traffic analysis, especially for protocol-level inspection such as HTTP.

* The `http` filter is useful to isolate web-related traffic out of thousands of packets in a capture.

* The GET method in HTTP reveals which resources were requested from a web server, and analyzing these can help detect:

  * Suspicious or unauthorized file access

  * Malware download attempts

  * Unusual browsing behavior

* Inspecting the `http.request.uri` field provides visibility into specific paths or pages requested, which is critical in incident response and threat hunting.

* Knowing how to combine filters enables faster and more precise analysis in large PCAP files.

## 📸 Screenshots

Screenshots from this lab can be found in the [screenshots](./screenshots) folder.
* Filtered `http` traffic

* Isolated `GET` requests

* Viewed `http.request.uri` details

---

✅ Challenge Repo: [30 Days SOC Challenge](https://github.com/0xrajneesh/30-Days-SOC-Challenge-Beginner)
✍️ Author: [Daniel Orji](https://www.linkedin.com/in/danielorji1542002)

---
