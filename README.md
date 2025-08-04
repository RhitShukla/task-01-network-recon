# task-01-network-recon (please refer the .nmap file for outputs)
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


I found 3 main devices my phone, laptop, and VM machine metasploitable
Then I studied about the ports and what common vulnerabilities can be found on the respective open ports.
Examples:
Host: 172.20.10.5
Host: 172.20.10.5 | MAC: 00:0C:29:B9:CE:4C | Vendor: VMware
Port                                   Service                                                                 Risk / Notes
21                                     ftp                                            Check for anonymous login or insecure file access
22                                     ssh                                            Brute-force or default credential attack possible
23                                     telnet                                         Insecure remote access (plaintext)
53                                     domain                                         Possible DNS misuse
80                                     http                                           Potential web vulnerabilities (XSS, LFI, etc.)
139                                    netbios-ssn                                    File share enumeration
445                                    microsoft-ds                                   SMBv1 vulnerabilities
514                                    shell                                          Insecure remote shell
And many more since Metasploitable is a vulnerable machine
