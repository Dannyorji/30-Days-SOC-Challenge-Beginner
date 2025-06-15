# 📅 Day 17 – Splunk Basics – DNS Log Analysis

## 🔍 What I Did

* Logged into the **Splunk web interface** on my Ubuntu machine to begin working with ingested logs.
* Explored and interacted with DNS log data already available within Splunk.
* Used Splunk’s **Search & Reporting app** to query and analyze log fields related to DNS traffic.
* Executed search queries to isolate important DNS-related fields such as:

  * `query`: the domain name being resolved
  * `orig_h`: the originating host IP making the request
  * `qtype`: the query type (e.g., A, AAAA, MX)
* Filtered logs using specific queries to extract meaningful insights from the dataset.
* Took relevant screenshots of the queries and results for documentation and future reference.

## 🧠 What I Learned

* Got hands-on practice with **Splunk Search Processing Language (SPL)** to extract fields and interpret DNS logs.
* Understood how Splunk can be used to **analyze DNS traffic** — a common vector for identifying suspicious activity like domain generation algorithms or C2 communications.
* Learned the significance of:

  * `query` field: indicates what domains are being accessed
  * `orig_h` field: shows the internal source of DNS requests
  * `qtype` field: helps determine the nature of the DNS request (A record, MX, etc.)
* Reinforced the role of **log analysis in threat detection** and how SOC teams use Splunk to monitor network behavior.

## 📸 Screenshots

Screenshots from this lab can be found in the [screenshots](./screenshots) folder.

---

✅ Challenge Repo: [30 Days SOC Challenge](https://github.com/0xrajneesh/30-Days-SOC-Challenge-Beginner)
✍️ Author: [Daniel Orji](https://www.linkedin.com/in/danielorji1542002)

---


