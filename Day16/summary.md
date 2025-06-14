# 📅 Day 16 – Setting up Splunk

## 🔍 What I Did

* Booted into my **Ubuntu** machine to set up a Security Information and Event Management (SIEM) tool — **Splunk**.

* Downloaded the **.tgz** package of Splunk Enterprise from the [official site](https://www.splunk.com/en_us/download/splunk-enterprise.html).

* Extracted the archive and moved the Splunk folder to the `/opt` directory for proper system organization:

  ```bash
  tar -xvzf splunk-*.tgz
  sudo mv splunk /opt/
  ```

* Initiated the Splunk setup using:

  ```bash
  sudo /opt/splunk/bin/splunk start --accept-license
  ```

* Created a Splunk admin username and password as prompted.

* Verified successful setup by accessing Splunk’s web interface on `http://localhost:8000`.

* Logged in and explored the Splunk dashboard — ready to ingest and analyze data logs.

## 🧠 What I Learned

* How to **install and configure Splunk** on a Linux system (Ubuntu).
* Understood the importance of **SIEM tools** in real-world SOC environments for log aggregation, real-time monitoring, and incident detection.
* Learned how to:

  * Download and extract Splunk’s Linux package.
  * Set permissions and move files to standard system locations.
  * Start Splunk for the first time and accept the license agreement.
  * Create secure login credentials.
* Gained hands-on exposure to **Splunk’s web interface**, where logs from different sources can be collected, searched, and visualized — an essential skill for SOC Analysts.

## 📸 Screenshots

Screenshots from this lab can be found in the [screenshots](./screenshots) folder.

---

✅ Challenge Repo: [30 Days SOC Challenge](https://github.com/0xrajneesh/30-Days-SOC-Challenge-Beginner)
✍️ Author: [Daniel Orji](https://www.linkedin.com/in/danielorji1542002)

---
