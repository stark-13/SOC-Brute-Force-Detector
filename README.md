# 🔐 SOC Brute Force Detection System

## 📌 Overview

This project is a simple Python-based security tool that simulates how a Security Operations Center (SOC) detects brute force attacks by analyzing login attempts.

It identifies suspicious behavior where multiple failed login attempts originate from the same IP address.

---

## 🚀 Features

* Detects repeated failed login attempts
* Flags potential brute force attacks
* Simple and easy-to-understand logic
* Demonstrates basic log analysis concepts used in SOC environments

---

## 🧠 How It Works

* The system processes login attempt data (IP address + status)
* Counts the number of failed attempts per IP
* If an IP exceeds a defined threshold (e.g., 3 failed attempts), it is flagged as suspicious

---

## 💻 Example Code

```python
logins = [
    ("192.168.1.1", "fail"),
    ("192.168.1.1", "fail"),
    ("192.168.1.1", "fail"),
    ("192.168.1.2", "success")
]

attempts = {}

for ip, status in logins:
    if status == "fail":
        attempts[ip] = attempts.get(ip, 0) + 1

for ip, count in attempts.items():
    if count >= 3:
        print(f"⚠️ Possible brute force attack from {ip}")
```

---

## 📊 Sample Output

```
⚠️ Possible brute force attack from 192.168.1.1
```

---

## 🎯 Purpose

This project demonstrates:

* Basic cybersecurity concepts
* Log analysis techniques
* Detection of brute force attacks in a SOC environment

---

## 🔧 Future Improvements

* Read logs from a file instead of hardcoding
* Add real-time monitoring
* Export alerts to a report
* Integrate with SIEM tools

---

## 👨‍💻 Author

[Your Name]
