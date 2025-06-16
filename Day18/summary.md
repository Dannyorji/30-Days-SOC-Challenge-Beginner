# 📅 Day 18 – Splunk Basics: SSH Log Analysis

## 🔍 What I Did

* Accessed the **Splunk web interface** on my Ubuntu system to begin analyzing SSH logs.
* Navigated to the **Search & Reporting** app and began querying logs relevant to **SSH activity**.
* Filtered for log events related to the **SSH daemon** using fields like:

  * `sshd`
  * `authentication`
  * `failed password`
  * `accepted password`
* Analyzed login attempts — both successful and failed — to spot possible brute-force activity or unauthorized access attempts.
* Focused on identifying:

  * Source IPs making login attempts
  * Usernames being targeted
  * Timestamps and frequency of access
* Took screenshots of the search queries and result patterns to document key insights.

## 🧠 What I Learned

* Learned how to **extract and analyze SSH authentication logs** from Linux systems using Splunk.
* Understood how **failed login patterns** can help detect brute-force or dictionary attacks.
* Recognized the value of specific log keywords in identifying:

  * Successful logins (`Accepted password`)
  * Failed logins (`Failed password`)
  * User enumeration attempts
* Learned how Splunk's powerful search capabilities allow SOC analysts to **track lateral movement and intrusion attempts** via SSH logs.
* Reinforced the importance of **log visibility** in investigating incidents and strengthening detection strategies.

## 📸 Screenshots

Screenshots from this lab can be found in the [screenshots](./screenshots) folder.

---

✅ Challenge Repo: [30 Days SOC Challenge](https://github.com/0xrajneesh/30-Days-SOC-Challenge-Beginner)
✍️ Author: [Daniel Orji](https://www.linkedin.com/in/danielorji1542002)

---

