# 🛡️ Cybersecurity Lab Portfolio

This repository showcases my hands-on cybersecurity lab work, combining core technical skills with investigative methodologies in a virtual environment. Each project simulates real-world attack, defense, or forensic analysis scenarios. The labs were conducted using VirtualBox, Kali Linux, Windows 10, and digital forensic tools like Autopsy and 7zip for file extraction.

---

## 📚 Table of Contents

1. [Virtual Network Lab Setup](#1-virtual-network-lab-setup)
2. [Mobile Device Forensics](#2-mobile-device-forensics)
3. [Firewall Traffic Segmentation (Coming Soon)](#3-firewall-traffic-segmentation-coming-soon)

---

## ✅ 1. Virtual Network Lab Setup

### 🧪 Objective:
To simulate an internal network environment between two virtual machines — Kali Linux (attacker) and Windows 10 (target) — for network-based reconnaissance and inspection.

### 🔧 Tools Used:
- Oracle VirtualBox
- Kali Linux (2025.1)
- Windows 10
- Nmap

### ⚙️ Configuration Summary:

| Component      | Details                           |
|----------------|------------------------------------|
| Type 2 Hypervisor | VirtualBox                     |
| Networking Mode | Internal Network                 |
| VM 1           | Kali Linux                        |
| VM 2           | Windows 10                        |
| Communication Test | ICMP Ping and Shared Folder |

### 📷 Screenshots:
- ✅ Successful ping from Kali to Windows  
  ![Ping Success Screenshot](https://github.com/Lone-Warlock/DSA-FINAL-PROJECT-I/blob/main/prelim_setup/06.%20KALI%20LINUX-WINDOWS.png)

- ✅ Shared directory (Windows to Kali)  
  ![Shared Folder Screenshot](https://github.com/Lone-Warlock/DSA-FINAL-PROJECT-I/blob/main/ACCESSED%20SHARED%20FOLDER.png)

### 📝 Notes:
- Static IP addresses were configured on both VMs
- Windows firewall was disabled to allow connectivity
- Folder sharing was enabled via Windows SMB

---

## ✅ 2. Mobile Device Forensics

### 🧪 Objective:
To conduct a forensic investigation of an Android disk image and document findings in a formal report.

### 🔧 Tools Used:
- Windows Autopsy GUI
- 7zip (.tar)
- Microsoft Word (for report formatting and PDF conversion)

### 🗃️ Key Findings:
| Artifact Type        | Evidence Extracted                         |
|----------------------|---------------------------------------------|
| SMS & Call Logs      | Evidence of both local and international calls   |
| Crypto wallet        | Bitcoin wallet address for transactional anonymity |
| Browser History      | Traces of search history revealing plans to obfuscate |

### 📷 Screenshots:
- Autopsy keyword hits  
  ![Autopsy Screenshot](https://github.com/Lone-Warlock/DSA-FINAL-PROJECT-I/blob/main/ANDROID_PHONE_DIGITAL_FORENSICS/EXHIBIT%20G.png)

- File system tree with evidence  
  ![File Tree](https://github.com/Lone-Warlock/DSA-FINAL-PROJECT-I/blob/main/ANDROID_PHONE_DIGITAL_FORENSICS/EXHIBIT%20F.png)

---

## 🛠️ 3. Firewall Traffic Segmentation (Coming Soon)

### 🧪 Objective:
To deploy a virtual pfSense firewall for segmenting traffic between Kali Linux (attacker) and Windows 10 (target) virtual machines, and test traffic inspection and filtering.

### 🔧 Tools Used:
- Oracle VirtualBox
- pfSense 2.6.0 ISO
- Kali Linux
- Windows 10

### 🛠️ Lab Setup Steps Attempted:
1. Created pfSense VM with two interfaces (WAN: NAT, LAN: Internal)
2. Assigned static IPs to both Kali and Windows on the LAN side
3. Verified communication between Windows and pfSense
4. Attempted to access pfSense Web GUI via browser from Windows

### ⚠️ Challenges Encountered:
- pfSense repeatedly froze or rebooted during startup
- "VM fault: pager read error" prevented installation twice after going through reinstallation process
- GUI became unreachable due to unstable VM state
- Kali lost network access after changing adapter settings

> Despite multiple configurations and troubleshooting attempts, a stable GUI connection to pfSense could not be maintained. The firewall's startup loop prevented full testing of firewall rules and filtering.

### 📷 Screenshots:
- ![VM Fault Error](https://github.com/Lone-Warlock/DSA-FINAL-PROJECT-I/blob/main/VIRTUAL%20FIREWALL%20IMPLEMENTATION/UNENDING%20LOADING%20PROCESS.png)
- ![Network Adapter Config](https://github.com/Lone-Warlock/DSA-FINAL-PROJECT-I/blob/main/VIRTUAL%20FIREWALL%20IMPLEMENTATION/pfSense.png)
- ![Successful Pings between the VMs](https://github.com/Lone-Warlock/DSA-FINAL-PROJECT-I/blob/main/VIRTUAL%20FIREWALL%20IMPLEMENTATION/INITIAL%20SUCCESSFULL%20RESPONSES.png)

### 📘 Key Learnings:
- Virtual network setup requires close adapter and MAC address monitoring
- pfSense must have correctly assigned storage and network controllers
- Snapshots are essential for rollback when a firewall breaks its boot loop
- Even partially working configurations expose networking principles in action

### 🔄 Next Steps:
I plan to reattempt the pfSense installation using a fresh ISO, increased RAM, and VirtualBox snapshots to preserve states. This will help complete the firewall configuration and filtering rules testing.


---

## 🧠 What I Learned

- How to configure and troubleshoot internal networks
- Realistic digital forensics techniques using Autopsy
- Basics of cyber evidence collection and documentation

---

## 📌 Author

**Dare Adelaja**  
Aspiring Network Security Engineer | Hands-on learner  

