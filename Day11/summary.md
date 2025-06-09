# 📅 Day 11 – Detecting Brute-Force Attacks via Event Logs and Firewall Analysis

## 🔍 What I Did

* Simulated a **brute-force attack** on a Windows machine using a Kali Linux system to generate **multiple failed login attempts**.
* Configured **RDP brute-force attack** using a Kali tool to repeatedly try login credentials against the Windows target.
* On the Windows machine, monitored the **Security Event Logs** using **Event Viewer**.
* Observed a spike in **Event ID 4625 (An account failed to log on)**, indicating multiple failed authentication attempts.
* Analyzed these entries to correlate them with the attack IP and login failure type (`Logon Type: 10` – RemoteInteractive).
* Implemented a **firewall rule** to block the attacking IP from further access, showcasing basic incident response.
* Took screenshots of:

  * The firewall rule created in Windows Defender Firewall with Advanced Security.
  * The attack session running on Kali Linux.
  * The series of failed login attempts recorded in Event Viewer.

## 🧠 What I Learned

* **Event ID 4625** is a key log source for identifying failed login attempts on Windows.
* Brute-force attacks can often be detected through rapid, repeated 4625 log entries with the same `TargetUserName` or from a single source IP.
* **Logon Type 10** signifies an RDP (Remote Desktop Protocol) attempt, useful for identifying remote brute-force efforts.
* Creating and applying **firewall rules** on Windows can help isolate and respond to such attacks quickly.
* Combining attacker behavior (via Kali) with defender visibility (via Event Logs and firewall) helps build better detection skills.

## 📸 Screenshots

Screenshots from this lab can be found in the [screenshots](./screenshots) folder.

---

✅ Challenge Repo: [30 Days SOC Challenge](https://github.com/0xrajneesh/30-Days-SOC-Challenge-Beginner)
✍️ Author: [Daniel Orji](https://www.linkedin.com/in/danielorji1542002)

---

