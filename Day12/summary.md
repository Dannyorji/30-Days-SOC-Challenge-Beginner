# 📅 Day 12 – Incident Response Basics: Suspicious Bash Script Execution

## 🔍 What I Did

* Booted into my **Ubuntu** machine to simulate suspicious activity.

* Downloaded and analyzed a **bash script** (`logger.sh`) that mimics the behavior of a malicious process.

* Switched to the **root user** to gain the necessary privileges for script execution using:

  ```bash
  sudo su
  ```

* Executed the script and monitored its behavior using:

  ```bash
  ps aux | grep logger.sh
  ```

* Observed the script persistently writing logs to `/tmp/logger.log`, mimicking stealthy background operations.

* Used `cat`, `tail`, and `less` to inspect the log file content.

* Identified the process ID (PID) of the script and terminated it using:

  ```bash
  kill -9 <PID>
  ```

* Verified that the script was no longer running and removed its associated files to complete the cleanup.

## 🧠 What I Learned

* Learned how to simulate and respond to suspicious bash script execution on a Linux system.
* Switching to **root** is often required to execute or investigate higher-privileged processes.
* Identified how a seemingly harmless script can act like malware by running persistently in the background and writing to system directories.
* Practiced **incident response basics**: detect → investigate → terminate → clean up.
* Reinforced the importance of monitoring `/tmp`, as it’s a common location used by attackers to store temporary payloads.
* Gained hands-on experience using Linux commands (`ps`, `grep`, `kill`, `cat`, etc.) to trace and handle suspicious activities.

## 📸 Screenshots

Screenshots from this lab can be found in the [screenshots](./screenshots) folder.

---

✅ Challenge Repo: [30 Days SOC Challenge](https://github.com/0xrajneesh/30-Days-SOC-Challenge-Beginner)
✍️ Author: [Daniel Orji](https://www.linkedin.com/in/danielorji1542002)

