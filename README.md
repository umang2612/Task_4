# Task_4
Setup and Use a Firewall on Windows
# 🔐 Firewall Configuration and Testing (Windows)

## 📌 Objective
Configure and test basic firewall rules to **allow** or **block** traffic on your system. Understand how firewalls filter network traffic and enforce system security.

---

## 🛠 Tools Used
- **Windows Defender Firewall (Advanced Security)**
- **PowerShell (Windows) / Terminal (Linux)**
- **Test-NetConnection**

---

## 🖥️ System Info
| Platform | OS         | IP Address      | Firewall Tool     |
|----------|------------|------------------|--------------------|
| Windows  | Windows 10/11 | 127.0.0.1 / hostname | Windows Defender Firewall |

---

## ✅ Steps Performed

### 🔹 Windows

#### 1. Open Firewall GUI
- `Start` → Search `Windows Defender Firewall with Advanced Security`

#### 2. List Current Rules
- Viewed **Inbound** and **Outbound** rules.

#### 3. Add Rule to Block Port 23 (Telnet)
- In **Inbound Rules** → `New Rule` → Port → TCP → Port `23` → Block → Apply to all profiles → Name: `Block Telnet`

#### 4. Test with PowerShell
```powershell
Test-NetConnection -Port 23 -ComputerName 127.0.0.1
