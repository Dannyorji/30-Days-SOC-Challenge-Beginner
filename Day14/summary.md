# 📅 Day 14 – Incident Response Basics: Suspicious PowerShell Activity

## 🔍 What I Did

* Booted into my **Windows** machine and prepared the environment for PowerShell logging.

* Enabled the following PowerShell logging features:

  * **Module Logging**
  * **Script Block Logging**
  * **Script Execution Logging**

* Simulated suspicious PowerShell behavior by launching PowerShell as **Administrator** and running the command:

  ```powershell
  Start-Process "notepad.exe" -ArgumentList "C:\Windows\System32\drivers\etc\hosts"
  ```

* Opened **Event Viewer** and navigated to:

  ```
  Applications and Services Logs > Microsoft > Windows > PowerShell > Operational
  ```

* Filtered logs for **Event ID 4103**, which captures detailed script block activity.

* Located the executed PowerShell command in the event log, confirming detection of the simulated attack.

* Followed basic **Incident Response (IR)** stages:

  * **Detection**: Identified suspicious behavior via PowerShell logging.
  * **Analysis**: Verified command intent and execution details.
  * **Containment & Eradication**: Killed the process and deleted the suspicious file if necessary.
  * **Recovery**: Ensured no residual activity remained.
  * **Lessons Learned**: Improved PowerShell restrictions and documentation.

* Enhanced system defenses by creating a **new outbound firewall rule** using Windows Defender Firewall to restrict potential abuse of PowerShell in future incidents.

## 🧠 What I Learned

* **PowerShell Event ID 4103** is valuable for detecting script execution activity and is essential for identifying malicious or suspicious behavior.
* Enabling **script block logging** provides visibility into all blocks of code executed by PowerShell, even if obfuscated.
* **Simulating attacker behavior** helps SOC analysts test visibility and improve response strategies.
* Learned the importance of combining detection with proper IR practices: containment, eradication, and prevention.
* Implementing **firewall rules** is an effective way to control and restrict risky behavior post-incident.

## 📸 Screenshots

Screenshots from this lab can be found in the [screenshots](./screenshots) folder.

---

✅ Challenge Repo: [30 Days SOC Challenge](https://github.com/0xrajneesh/30-Days-SOC-Challenge-Beginner)
✍️ Author: [Daniel Orji](https://www.linkedin.com/in/danielorji1542002)

---

