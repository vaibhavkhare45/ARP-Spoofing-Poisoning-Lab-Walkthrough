# ARP-Spoofing-Poisoning-Lab-Walkthrough

This project demonstrates a **Man-in-the-Middle (MITM) attack** using **ARP Spoofing/Poisoning**.  
The attack is performed in a controlled lab setup with **Kali Linux (attacker)** and **Windows 7 (victim)** running on a virtual environment.

⚠️ **Disclaimer:** This walkthrough is for **educational purposes only**. Do not attempt on real networks without permission.  

---

## 🖥️ Lab Setup  

- **Attacker:** Kali Linux  
- **Victim:** Windows 7  
- **Network:** NAT / Host-Only Adapter  
- **Tool Used:** `arpspoof` (part of `dsniff` package)  

---

## 🧩 What is ARP?  

- **ARP (Address Resolution Protocol):** Maps an IP address to a MAC address on a LAN.  
- Example: `192.168.152.2 → 00:11:22:33:44:55`  

---

## ⚡ Attack Overview  

1. Attacker sends **fake ARP replies** to victim & router.  
2. Victim thinks attacker = router.  
3. Router thinks attacker = victim.  
4. All traffic flows **through attacker’s machine** (MITM).  

---

📊 Attack Flow
Windows 7 (Victim) <---> Kali Linux (Attacker / MITM) <---> Router (Gateway)

---

## 📸 Screenshots  

ARP spoofing command execution
![Screenshot 1](./Screenshot%202025-08-25%20221401.png)  
![Screenshot 2](./Screenshot%202025-08-25%20221437.png)

Enable IP Forwarding

![Screenshot 3](./Screenshot%202025-08-25%20221503.png)  

Sniffed traffic logs (victim’s HTTP requests)
![Screenshot 4](./Screenshot%202025-08-25%20221536.png)  

---

🔒 Defense Against ARP Poisoning

Use Static ARP entries where possible.

Enable Dynamic ARP Inspection (DAI) on managed switches.

Use VPNs / HTTPS to encrypt traffic.

Employ IDS/IPS tools (e.g., Snort, Suricata) to detect ARP anomalies.

---

✨ Author

👨‍💻 Created by Vaibhav Khare
