Computer Networks
---
A LAN would be Home wifi as its small and covers a limited area. 

A WAN would be like the internet as it connects home, schools and businesses worldwide

<img width="1783" height="848" alt="image" src="https://github.com/user-attachments/assets/3c228866-b276-4737-b7ac-e30c925fd999" />

The WAN concept basically connects a multiple of LANs to enable communication and data transfer over long distances

**Switches** operate as a manager for your local network. It connects multiple devices within the same network (printer, computer etc) - it ensures that data flows smoothly between the devices preventing congestion and ensuring efficiate communication

**Router** play the role of a traffic cop directing traffic between different entworks essentially direct traffic between diffrent networks. The role of a router at home is connecting your home network to the internet, it ensures data gets to the right place 
when browsing the internet or watching videos. - The two roles it plays is directing traffic in the network and connecting to different networks.

**Firewals** is basically a security guard for your network as it monitors incoming and outgoing network traffic based on the rules set in place. It does two things, protects the network from unauthorised access and monitoring incoming/outgoing network traffic. 

These **there** components form the backbone of any network.

<img width="1810" height="860" alt="image" src="https://github.com/user-attachments/assets/544d7e6b-4a83-421a-aed0-44423b882c09" />

**IP Addr** oe internet protocol address is a unique identifier assigned to each device on a network. Allows devices to Locate and Communicate with each other. There are two types of IP addresses such as IPv4 and IPv6, the most common one is IPv4 and start with 192.168...

IPv4- They are 32 bit addresses, written in Four decimal numbers separated by dots and each group and go up to 255 providing up to 4.3 billion unique addresses. With how rapid the internet is growing, IPv4 address are becoming scarce (starting to run out) which is 
where IPv6 Addresses come in.

IPv6- are 128 bit addresses. that provider a much wider pool of addresses. These are written in 8 groups of four hexadecimal digits separated by colons. Without IP addresses, devices wouldn't know where to send or receive data.  

<img width="1682" height="827" alt="image" src="https://github.com/user-attachments/assets/db2154b8-7f22-4bad-b696-0dff1f6f9045" />

**MAC Addr** or otherise known as the Media Access Control Address is a unique identifier assigned to a network interface, meaning each device has it's own unique MAC address. MAC addr are 48 bit addresses that look something like the below picture. This network protocl 
operates in the data link layer and facilitates device identification within a local network. It also crucial for ensuring your laptop connects to the correct router and not a neighbours one. 

<img width="1592" height="648" alt="image" src="https://github.com/user-attachments/assets/897467f3-3796-446a-863e-5933818561da" />

**Ports** are logical doors on your device, each door is numbered and each door is used for a specific type of network communications e.g. HTTP goes through port 80 and port 443 for HTTPS.

**Protocols** are basically the rules of the road for data transmission. They define how data is formatted and transmitted across a network (SFTP, FTP, SMTP). These protocols ensure devices can communiate effectively by following the same set of rules.
- Think of it as languages devices uses to communicate with each other.

The importance of Ports in networking is that they ensure data gets to the right application on your device whilst protocols make sure the data is properly formatted and understandable they are essential for smooth and effecient communication.

<img width="1704" height="777" alt="image" src="https://github.com/user-attachments/assets/4011e05d-655b-4d9e-9928-190d08970805" />

**TCP** The transmission control Protocol is the postman of the networking world. It makes sure that data from one device, reaches it's destination accurately and in the correct order. Before any data is sent, a connection needs to be established for this to accomplish.
TCP requires a 3 step ***handshake*** process where the two device essentially agree for the transfer of data. Reliable data source

A benefit of TCP is that the order of data being sent being the exact same. Basically meaning that it won't send a a later message first rather it keeps the order the same. Error checking and flow control is another main function of TCP as it checks for errors and control the flow of data to prevent congestion. TCP is used whenever two devices need to exchange data back and forth e.g. web browsing, emailing, file transfers.

<img width="1776" height="818" alt="image" src="https://github.com/user-attachments/assets/f5a1f217-00ba-47ce-84f9-6791adabcb75" />

**UDP** User Datagram Protocol is used to send and receive data. This is much faster than TCP however less reliable, it is straight forward and no prior communication is needed. UDP's function are suitable for real-time applications like gaming and video streaming, in some cases it also used for VPN connections as speed can be more essential that reliability and finally used for DNS lookup.

<img width="1796" height="830" alt="image" src="https://github.com/user-attachments/assets/1bc464b1-0a4a-4ed2-b1d6-0371c2eb4dd8" />

**Both TCP and UDP are layer 4 protocols in the OSI model.**

<img width="1749" height="879" alt="image" src="https://github.com/user-attachments/assets/7b5ea601-2552-4951-95fc-88532971ac8d" />

