# Date :24/07/2026
# Name: Mathan Kailash S
# Reg No: 212223060156
## Ex.-No-2-Interconnecting-Two-LANs-Using-a-Router-Basic-Router-Configuration


# Objective
To configure a router to connect two separate LANs and enable communication between them using static IP addressing.
________________________________________
# Apparatus/Tools Required
•	Cisco Packet Tracer<br>
•	2 PCs<br>
•	2 Switches<br>
•	1 Router (e.g., 1841 or 2911)<br>
•	Straight-through cables<br>
________________________________________
# Network Topology Diagram

 Description:<br>
•	PC0 → Switch0 → Router (FastEthernet0/0)<br>
•	PC1 → Switch1 → Router (FastEthernet0/1)<br>
<img width="1920" height="1080" alt="Screenshot 2026-07-24 134120" src="https://github.com/user-attachments/assets/51445765-8d4f-41b1-8e87-e5c047b1968c" />
________________________________________
# IP Addressing Table
Device	Interface	IP Address	Subnet Mask<br>
PC0	NIC	192.168.1.10	255.255.255.0<br>
PC1	NIC	192.168.2.10	255.255.255.0<br>
Router0	FastEthernet0/0	192.168.1.1	255.255.255.0<br>
Router0	FastEthernet0/1	192.168.2.1	255.255.255.0<br>
________________________________________
# Procedure
1.	Open Cisco Packet Tracer and add 2 PCs, 2 Switches, and 1 Router.
2.	Connect each PC to a switch, and each switch to the router using straight-through cables.
3.	Assign IP addresses to both PCs according to the IP table.
4.	Configure the router interfaces:
o	FastEthernet0/0 → 192.168.1.1
o	FastEthernet0/1 → 192.168.2.1
5.	Use no shutdown on both router interfaces to activate them.
6.	Set each PC’s default gateway:<br>
o	PC0 → 192.168.1.1<br>
o	PC1 → 192.168.2.1<br>
7.	Test connectivity using ping from PC0 to PC1.<br>
________________________________________
# Commands Used (Router CLI)
bash<br>
CopyEdit<br>
Router> enable<br>
Router# configure terminal<br>
Router(config)# interface fastethernet0/0<br>
Router(config-if)# ip address 192.168.1.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>

Router(config)# interface fastethernet0/1<br>
Router(config-if)# ip address 192.168.2.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>
________________________________________
# Output (Screenshots)
<img width="1920" height="1080" alt="Screenshot 2026-07-24 134200" src="https://github.com/user-attachments/assets/827f034a-967e-4e37-a386-a8cfbbacc75b" />
<img width="1920" height="1080" alt="Screenshot 2026-07-24 134212" src="https://github.com/user-attachments/assets/c0e37b41-4c6c-466d-88ae-597a98921ff2" />
<img width="1920" height="1080" alt="Screenshot 2026-07-24 134527" src="https://github.com/user-attachments/assets/9a5ebf5c-19f9-4d8b-91ab-a1162ff56e9d" />
<img width="1920" height="1080" alt="Screenshot 2026-07-24 134008" src="https://github.com/user-attachments/assets/60f2e5d0-2d63-478f-ade9-1bba49309151" />
<img width="1920" height="1080" alt="Screenshot 2026-07-24 134045" src="https://github.com/user-attachments/assets/a636655d-eb5c-4b55-bf5c-7babf101e760" />



•	Router CLI configuration<br>
•	IP configurations on PCs<br>
•	Successful ping between PC0 and PC1<br>
________________________________________
# Result
Successfully configured a router to connect two LANs. Communication between PC0 and PC1 across different networks was tested and verified.

