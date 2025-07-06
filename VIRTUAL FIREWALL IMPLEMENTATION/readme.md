# 🔐 Cybersecurity Lab: Firewall Traffic Segmentation with pfSense

This section documents my attempt to deploy and configure a pfSense virtual firewall to inspect, route, and filter traffic between Kali Linux and Windows 10 virtual machines in a controlled lab environment using Oracle VirtualBox.

---

## 🎯 Objective

To enhance the virtual lab with a functional firewall, providing traffic inspection and segmentation between internal hosts (Kali & Windows 10).

---

## 🧰 Tools 

- Oracle VirtualBox (Type 2 hypervisor)
- pfSense 2.6.0 ISO
- Kali Linux 2025.1 (Attacker)
- Windows 10 VM (Target)
- Internal Network + NAT adapters

---

## 📡 Network Setup & IP Addresses

| Machine         | Interface     | IP Address      | Adapter Type      |
|-----------------|---------------|------------------|--------------------|
| *pfSense WAN* | em0 (Adapter 1) | 10.0.2.15 (DHCP) | NAT (external access) |
| *pfSense LAN* | pcn0 (Adapter 2) | 192.168.1.1      | Internal Network     |
| Kali Linux      | Adapter 1       | 192.168.1.102     | Internal Network     |
| Windows 10      | Adapter 1       | 192.168.1.11     | Internal Network     |

---

## ⚙ Configuration Steps Attempted

1. Created pfSense VM with 2 network adapters:  
   - Adapter 1: NAT (WAN)  
   - Adapter 2: Internal Network (LAN)
2. Assigned static IPs to Kali and Windows in the same LAN subnet (192.168.1.0/24)
3. Successfully pinged pfSense from Windows
4. Attempted access to pfSense Web UI from Windows browser (https://192.168.1.1)
6. Kali briefly connected but later lost network communication
7. Faced repeated reboots and startup hangs in pfSense VM
8. Created and restored snapshots to preserve configuration attempts

---

## ⚠ Challenges Faced

- VM fault: pager read error when rebooting pfSense
- pfSense GUI becoming unresponsive after initial boot
- Failed to connect to the internet while trying a regular Google search to test the WAN access
- Adapter names and MAC assignments were inconsistent
- Kali lost connection while Windows maintained access
- Grayed-out network options prevented interface reassignment
- No access to web configuration from Kali
- No web configuration access from Windows
Despite successful ping from Windows, I couldn’t consistently reach or configure the pfSense Web GUI.

---

## 📷 Screenshots

> Screenshots are in the .png files under the virtual firewall inplementation folder

- ![Pager Read Error](https://github.com/Lone-Warlock/DSA-FINAL-PROJECT-I/blob/main/VIRTUAL%20FIREWALL%20IMPLEMENTATION/UNENDING%20LOADING%20PROCESS.png)
- ![Successful pings between the VMs](https://github.com/Lone-Warlock/DSA-FINAL-PROJECT-I/blob/main/VIRTUAL%20FIREWALL%20IMPLEMENTATION/pfSense.png)
- ![Kali Adapter Settings](https://github.com/Lone-Warlock/DSA-FINAL-PROJECT-I/blob/main/VIRTUAL%20FIREWALL%20IMPLEMENTATION/pfSense.png)

---

## 💡 Lessons Learned

- The importance of network adapter consistency across all VMs
- How pfSense interfaces are mapped (WAN = em0, LAN = pcn0)
- Virtual networking quirks in VirtualBox and the value of snapshots
- Even partial firewall configuration gives insights into routing behavior

---

## 🔁 Next Steps

I plan to:
- Reinstall pfSense from scratch using improved disk and RAM settings
- Document successful traffic filtering using firewall rules
- Integrate logs and rule-based blocking demonstrations

---

