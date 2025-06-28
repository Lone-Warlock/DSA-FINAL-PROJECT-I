# 🧪 Cybersecurity Lab Environment for DSA Project (Kali ↔ Windows)

This project sets up a realistic cybersecurity lab for practicing ethical hacking, enumeration, and system interaction between virtual machines.

---

## 📌 Project Objectives

1. ✅ Install and configure a Type 2 hypervisor
2. ✅ Deploy two virtual machines:
   - Kali Linux (Attacker)
   - Windows 10 (Target)
3. ✅ Establish internal virtual networking between the two VMs
4. ✅ Verify connectivity through:
   - ICMP (Ping) testing
   - SMB shared folder access
   - Service and port enumeration using Nmap 

---

## 🏗️ Environment Setup

| Component         | Description               |
|------------------|---------------------------|
| Hypervisor       | Oracle VM VirtualBox      |
| Attacker Machine | Kali Linux (latest)       |
| Target Machine   | Windows 10 Pro (x64)      |
| Networking Mode  | Internal Network (VirtualBox-only network) |

---

## 🧪 Lab Phases

### 1️⃣ Preliminary Setup

- Assigned static IPs to both VMs
- Verified internal-only connectivity
- Firewall temporarily disabled on Windows for unrestricted access

📄 See: [`prelim-setup/`](prelim_setup)

---

### 2️⃣ Connectivity Verification

- Performed ping tests between Kali and Windows VMs
- Screenshots and IP configuration included

- WINDOWS-KALI
 ![Windows-Kali`](https://github.com/Lone-Warlock/DSA-FINAL-PROJECT-I/blob/main/prelim_setup/WINDOWS-KALI%20LINUX.png)
- KALI-WINDOWS
 ![Kali-Windows](https://github.com/Lone-Warlock/DSA-FINAL-PROJECT-I/blob/main/prelim_setup/KALI%20LINUX-WINDOWS.png)

---

### 3️⃣ Shared Directory Access (SMB)

- Configured shared folder on Windows
- Accessed from Kali using `smbclient`

📄 See: [`smb-access.md`](https://github.com/Lone-Warlock/DSA-FINAL-PROJECT-I/blob/main/prelim_setup/SMB_ACCESS.md)

---

### 4️⃣ Service Enumeration

- Used Nmap to discover open ports and services on Windows
- Documented the tool and outputs used

📄 See: [`service-enumeration.md`](https://github.com/Lone-Warlock/DSA-FINAL-PROJECT-I/blob/main/SERVICE-ENUMERATION.md)

---

## 🔒 Post-Test Cleanup

- Windows firewall re-enabled using:

```cmd
netsh advfirewall set allprofiles state on
