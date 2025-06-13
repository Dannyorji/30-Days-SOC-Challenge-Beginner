# 📅 Day 15 – Incident Response Basics: Linux Suspicious Process

## 🔍 What I Did

* Booted into my **Ubuntu** machine and switched to the **root** user to simulate a suspicious process.

* Ran the following command to simulate persistent outbound communication with a remote server:

  ```bash
  nohup bash -c 'while true; do curl http://45.13.220.98/ping >/dev/null 2>&1; sleep 30; done' &
  ```

* Used the `netstat` command to detect active outbound connections:

  ```bash
  netstat -plant
  ```

  This revealed a suspicious connection to the IP `45.13.220.98`.

* Investigated the process making the connection using:

  ```bash
  ps aux | grep 45.13.220.98
  ```

  This helped identify the **PID** (Process ID) associated with the malicious curl loop.

* Terminated the suspicious process using:

  ```bash
  kill -9 <PID>
  ```

* Took action to prevent further communication by blocking the outbound IP with **UFW**:

  ```bash
  ufw deny out to 45.13.220.98
  ```

## 🧠 What I Learned

* How to simulate and analyze a **suspicious background process** on a Linux system using `nohup` and `curl`.
* Learned to detect **active connections** with `netstat` and trace them back to their processes using `ps aux` and `grep`.
* Understood how to **contain and eradicate** malicious activity using `kill -9` and network-level blocking with `ufw`.
* Reinforced the **Incident Response lifecycle**:

  * **Detection**: Identified abnormal persistent connections.
  * **Analysis**: Investigated the origin and nature of the process.
  * **Containment & Eradication**: Killed the rogue process and blocked its destination IP.
  * **Recovery**: Ensured the system no longer communicated with the malicious IP.
  * **Lessons Learned**: Practice showed how quickly a SOC analyst must act to mitigate threats.

## 📸 Screenshots

Screenshots from this lab can be found in the [screenshots](./screenshots) folder.

---

✅ Challenge Repo: [30 Days SOC Challenge](https://github.com/0xrajneesh/30-Days-SOC-Challenge-Beginner)
✍️ Author: [Daniel Orji](https://www.linkedin.com/in/danielorji1542002)

---

