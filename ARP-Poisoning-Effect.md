🧪 Step 3: ARP Poisoning Effect

✅ Normal ARP Table (Before Attack)

Victim (Win7)

192.168.*.* → 00:11:22:33:**:**   (Router MAC)


Router

192.168.1.*** → AA:BB:CC:DD:**:**   (Victim MAC)

❌ Poisoned ARP Table (After Attack)

Victim (Win7)

192.168.1.1 → 11:22:33:44:**:**   (Attacker MAC as Router)


Router

192.168.1.*** → 11:22:33:44:**:**   (Attacker MAC as Victim)


📌 Result: All traffic passes through attacker → enabling sniffing, credential theft, or injection attacks.

🔒 Defense Against ARP Poisoning

Use Static ARP entries where possible.

Enable Dynamic ARP Inspection (DAI) on managed switches.

Use VPNs / HTTPS to encrypt traffic.

Employ IDS/IPS tools (e.g., Snort, Suricata) to detect ARP anomalies.
