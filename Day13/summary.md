# 📅 Day 13 – Incident Response Basics: Malicious Cron Jobs

## 🔍 What I Did

* Booted into my **Ubuntu** machine to investigate scheduled tasks.

* Checked for active **cron jobs** using:

  ```bash
  crontab -l
  ```

* Discovered a suspicious cron job entry scheduled to run a hidden script every minute:

  ```bash
  * * * * * /tmp/.malicious.sh
  ```

* Located the malicious script stored in `/tmp/.malicious.sh` by inspecting the cron job path.

* Analyzed the contents of the script using:

  ```bash
  cat /tmp/.malicious.sh
  ```

* Observed that the script echoed repetitive messages to a file, simulating unwanted or malicious activity.

* Removed the malicious cron job entry using:

  ```bash
  crontab -e
  ```

* Deleted the suspicious script file from the system with:

  ```bash
  rm /tmp/.malicious.sh
  ```

* Verified that the cron job no longer existed by rechecking with `crontab -l`.

## 🧠 What I Learned

* Understood how attackers can use **cron jobs** to schedule and persist malicious activity on a system.
* Learned how to list, inspect, and edit user-specific cron jobs using `crontab`.
* Gained insight into how hidden or temporary files (`/tmp/.malicious.sh`) can be used for stealth operations.
* Practiced the full **incident response cycle**: detect → investigate → eliminate → verify.
* Recognized the importance of regularly auditing cron jobs as part of system monitoring and threat detection.

## 📸 Screenshots

Screenshots from this lab can be found in the [screenshots](./screenshots) folder.

---

✅ Challenge Repo: [30 Days SOC Challenge](https://github.com/0xrajneesh/30-Days-SOC-Challenge-Beginner)
✍️ Author: [Daniel Orji](https://www.linkedin.com/in/danielorji1542002)

---

