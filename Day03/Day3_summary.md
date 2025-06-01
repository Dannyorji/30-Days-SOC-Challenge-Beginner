# Day 3 – PowerShell Logging & Event ID 4103

## 🔍 Activity Summary
- Executed a PowerShell command to open the `hosts` file using Notepad:
  ```powershell
  Start-Process notepad.exe -ArgumentList "C:\Windows\System32\drivers\etc\hosts"
  ```
- This triggered **Event ID 4103** in the **Microsoft-Windows-PowerShell/Operational** log.
- Used **Event Viewer** to filter and view the event under:
  ```
  Applications and Services Logs > Microsoft > Windows > PowerShell > Operational
  ```

## 🧠 Key Takeaways
- **Event ID 4103** logs detailed information about PowerShell command execution, including:
  - The actual command and its parameters
  - The user who ran the command
  - Execution context (e.g., PowerShell host)
- Useful for detecting:
  - Suspicious PowerShell usage
  - Post-exploitation activities
  - Initial stages of malware execution or enumeration

## 🛡️ Relevance to SOC
- Event ID 4103 is **crucial for threat hunting** and **incident investigation** in Windows environments.
- Helps detect stealthy PowerShell-based attacks used by adversaries.

## 📸 Screenshot Reference
- Screenshots from this lab can be found in the [screenshots](./screenshots) folder.

---

✅ Challenge: [30 Days SOC Challenge (Beginner)](https://github.com/0xrajneesh/30-Days-SOC-Challenge-Beginner)  
✍️ Author: [Daniel Orji](https://www.linkedin.com/in/danielorji1542002)
