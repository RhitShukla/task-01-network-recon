# task-01-network-recon
TCP SYN Scan lab for devices 
Tools I Used 
- 'nmap' (stealth scan mode also with some modification to fast up the process)
- 'wireshark' (packet analysis)
- Linux terminal
- Metasploitable (A deliberately vulnerable Virtual Machine to practice testing)

#Scan Command I Used
sudo nmap -sS -T4 -min-rate 1000 --open -oA scan_report 172.20.10.0/24
-sS (for TCP SYN scan)
-T4 (Timing template- speeds up the scan)
-min-rate 1000 (sends at least 1000 packets/sec)
--open (Only shows hosts with at least one open port)
-oA scan_report (output in all 3 formats regular text, xml, and grep-friendly)

