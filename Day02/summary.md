# 📅 Day 2 – Log Analysis Basics: Windows Security Logs

## 🔍 What I Did

- Created a **new local user** account named `daxuser1` on my Windows system.
- Opened **PowerShell** and attempted a login with an incorrect password using the command:

                  `net use \127.0.0.1\IPC$ /user:daxuser1 WrongPassword`

- This triggered a **failed login attempt**, which generated an event with **Event ID 4625** in the Windows Security logs.
- Opened **Event Viewer** and navigated to:
Windows Logs > Security

- Filtered for **Event ID 4625** and found the exact failed logon event tied to the `daxuser1` account.

## 🧠 What I Learned

- **Event ID 4625** is triggered when a login attempt fails — useful for detecting brute-force attacks, unauthorized access attempts, or misconfigured systems.
- The `net use` command can be used to simulate login attempts, helping in testing log monitoring and alerting setups.
- Important fields in the 4625 log:
- `Account Name`: identifies the user that tried to log in
- `Failure Reason`: indicates why the login failed
- `Logon Type`: helps determine how the login was attempted (interactive, remote, etc.)
- Filtering specific Event IDs in Event Viewer saves time when investigating security-related incidents.

## 📸 Screenshots

Screenshots from this lab can be found in the [screenshots](./screenshots) folder.

---

✅ Challenge Repo: [30 Days SOC Challenge](https://github.com/0xrajneesh/30-Days-SOC-Challenge-Beginner)  
✍️ Author: [Daniel Orji](https://www.linkedin.com/in/danielorji1542002)
