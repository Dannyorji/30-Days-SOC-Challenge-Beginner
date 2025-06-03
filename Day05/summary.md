# 📅 Day 5 – Log Analysis Basics: Linux Auth Logs
## 🔍 What I Did
Used Kali Linux (attacker) to simulate a brute-force SSH attack on an Ubuntu machine (victim) using Hydra.

* Created a password.txt file containing a list of random passwords.

* Initiated the attack with the command:
    ```bash
     hydra -l testuser -P password.txt ssh://<Victim-IP>
    ```
* Switched to the victim machine:
    * Navigated to the authentication log directory:
      
         `cd /var/log`
      
* Used the command below to monitor authentication attempts in real time:
  
         `tail -f auth.log`
  
* Identified brute-force attempts through multiple failed SSH login entries.

* Filtered failed attempts using:
  
         `grep "Failed password" auth.log`
  
* This allowed me to isolate and analyze only the relevant suspicious activity.

## 🧠 What I Learned
* `Hydra` can automate brute-force attacks against SSH, which is useful for testing defenses.

* `auth.log` in Linux stores authentication events, including successful and failed SSH login attempts.

* Real-time log monitoring using `tail -f` helps detect ongoing attacks.

* `grep` is powerful for filtering logs and removing noise.

* Detecting repeated failed SSH logins from the same IP is a strong sign of a brute-force attempt, which SOC analysts should act on quickly.

## 📸 Screenshots

Screenshots from this lab can be found in the [screenshots](./screenshots) folder.

---

✅ Challenge Repo: [30 Days SOC Challenge](https://github.com/0xrajneesh/30-Days-SOC-Challenge-Beginner)
✍️ Author: [Daniel Orji](https://www.linkedin.com/in/danielorji1542002)

---
