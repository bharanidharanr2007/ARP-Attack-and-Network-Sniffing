# ARP-Attack-and-Network-Sniffing
# Explore Network Sniffing and ARP Attacks

# AIM:

To explore network sniffing and ARP Attacks

## STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:


### Step 3:
Open terminal and try execute some kali linux commands

## ARP Attacks:  
ARP spoofing: A hacker sends fake ARP packets that link an attacker's MAC address with an IP of a computer already on the LAN. 
Boot kali and Windows7 virtual machines.
In windows 7 give the command arp -a
## OUTPUT:

<img width="768" height="652" alt="image" src="https://github.com/user-attachments/assets/d58c7236-7e34-40e4-a009-f808f8218a38" />

The image shows a Windows Command Prompt displaying the result of the arp -a command, which lists the ARP (Address Resolution Protocol) cache entries for the computer’s network interfaces. Two interfaces are visible: 169.254.111.105, which is a self-assigned APIPA address indicating the system may not have received an IP from a DHCP server, and 192.168.56.1, which appears to be a virtual network adapter commonly used by virtualization software. The table includes Internet (IP) addresses, corresponding physical (MAC) addresses, and entry types marked as either dynamic or static. Several multicast and broadcast addresses such as 224.0.0.x and 255.255.255.255 are also present, which are standard networking entries. Overall, the output provides information about devices and address mappings on the local network and is commonly used for network troubleshooting and monitoring.


From kali linux issue the command :
sudo arpspoof -i eth0 -t <target system> <gateway>
## OUTPUT:

<img width="815" height="470" alt="image" src="https://github.com/user-attachments/assets/390900a4-77ef-406d-a83d-40cb38153ba7" />
.
.
.

<img width="816" height="464" alt="image" src="https://github.com/user-attachments/assets/9f2077ff-9b1c-4e74-884f-3cea2e6a4ebd" />

The images show the Ettercap network analysis tool running on a Linux system, displaying the results of a network host scan in the “Host List” window. Two hosts were discovered on the local network with IP addresses 10.0.2.2 and 10.0.2.3, along with their corresponding MAC addresses. The lower console section indicates that Ettercap started unified sniffing mode, randomized hosts for scanning, scanned the subnet for 255 hosts, and successfully added two hosts to the list. In the second image, the discovered hosts were assigned as TARGET1 and TARGET2, indicating preparation for network traffic analysis or testing between the selected systems.


In Kali issue the following commands:
sudo dsnifff
## OUTPUT:

<img width="1919" height="1070" alt="image" src="https://github.com/user-attachments/assets/aa23517c-712c-43d0-afc8-858d4d074525" />

The image shows a network packet analysis captured using the software Wireshark on a Linux-based system. The ARP (Address Resolution Protocol) filter is applied to monitor ARP traffic on the network interface eth0. Multiple ARP reply packets are displayed between source and destination MAC addresses, repeatedly indicating “duplicate use of 10.0.2.3 detected,” which suggests an IP address conflict in the network where more than one device is attempting to use the same IP address. The packet details section at the bottom provides Ethernet II and ARP protocol information, while the hexadecimal view displays the raw packet data. Overall, the screenshot demonstrates network troubleshooting and packet inspection used to identify ARP-related communication issues and duplicate IP conflicts within a local network.


## RESULT:
The kali linux tools for ARP Attack and Network Sniffing were identified successfully
