# DEMO
Repo for in-person demonstrations to hold any files and related wikis.
<br/><br/>
## 10/25
### Accessing the Network
Starting things off with a simple packet capture.\
<br/><br/>
The pcap file was captured using a Flipper Zero with Marauder WiFi dev board enabled doing a sniff forced de-auth attack.\
The pcap may be verified with wireshark using the 'eapol' filter.\
Using the hashcat web tool @ https://hashcat.net/cap2hashcat/, the pcap file containing authentication tokens from various sources to the network was converted into an hc22000 file that hashcat can read.\
**Note:** *The captures may not be able to be done live as the AP set-up for the demo is rather slow. They were captured using a more robust network that was set up for the capture only.* 
<br/><br/>
With this, an attacker can attempt to crack the password and gain access to the wireless network. As this is for demonstration purposes only, the password used is easily cracked with a password list. It is best to use the rockyou.txt file for this, but likely any should suffice.\

After gaining access to the network, the rest of the demo may ensue.
<br/><br/>

### Reconnaissance
Using the cracked password, connect to the 'ESP32-AP' access point set up. This is the simple network all devices for this demo have been configured to be connected to.\
The goal is to use Kali-enabled tools for red-team exploitation of a server. The server in question will either be a dedicated Raspberry Pi or computer for the demo.\

#### Steps:
Verify an IP address was given.\
Do a scan on the subnet.\
For this demo, 'server.local' is the working hostname for a target device that can be attacked. Do an nmap scan to see which ports are open. 
```bash
nmap <target ip>
```
*Question:* *Does this make too much noise? If so, what can we do about it?*
<br/><br/>
### Attack 
Knowing what is open and where vulnerabilities may lie, an attacker can begin to map out an attack.

TODO:
* The rest
  
