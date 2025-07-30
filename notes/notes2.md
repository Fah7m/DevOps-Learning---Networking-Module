OSI Model 
---
There are 7 layers in the OSI model which each handle different things in networking.

<img width="1552" height="1021" alt="image" src="https://github.com/user-attachments/assets/615dfe0a-95de-4881-bb34-bb78bd8ad5fb" />

**Physical Layer** - This layer handles the hardware connection such as Cable, Switches and Network Interface Cards 

<img width="1206" height="906" alt="image" src="https://github.com/user-attachments/assets/9d8d7c3d-86f1-4a9f-b28b-c4735b33ee4c" />

**Data link Layer** This layer is responsible for node to node data transfer - the traffic cop that ensures data is sent and received correctly between different network nodes. This layer is where the data packets are organized and some of the components that are used are
MAC addresses, Switches and Bridges 

<img width="1223" height="904" alt="image" src="https://github.com/user-attachments/assets/4cdfd460-cb27-40f0-a59c-ff859de14693" />

**Network Layer** is responsible to determine how the data is sent to the receipient. It also manages packet forwarding, including routing through different routers. It essentially decides the best path of travel across multiple networks so that the data reaches its destination. Components that are used are IP addresses and routers. The data at this layer are organized into packets, and this is where IP addresses come in as they handle where the packets go, and the routers are the compnents that allow this to happen. 

<img width="1242" height="883" alt="image" src="https://github.com/user-attachments/assets/52ce4f38-41dc-4f17-9e9c-35c0c81885ad" />

**Transport Layer** is responsible for providing reliable data transfer services to the upper layers. This is basically the delivery services that ensures the data arrives safely and in the correct sequence. The protocols that are used here are TCP and UDP. 

<img width="1234" height="871" alt="image" src="https://github.com/user-attachments/assets/a453de59-ff4c-41cd-8416-e0b7ef5eed23" />

**Session layer** is responsible for three things which is establishing, managing and terminating sessions. This means, gettings a session started like when you log into a website, and maintaining connections means keeping the session alive and finally terminating the session when you're done e.g. logging out or closing the tab. Components for this are management protocols like RPC and NetBIOS> 

<img width="651" height="481" alt="image" src="https://github.com/user-attachments/assets/f4dbb179-4814-4e6e-b3ab-afb9b1747e70" />

**Presentation Layer** is known as the syntax layer meaning data that is being sent is in a readable or usable format. It's like a translator that converts the data into a format in which the application layer can understand. This can handles encryption to ensure the security of the data e.g. plain text converted into encrypted text and data formatting for things like JPEG or MPEG files converted into a readable format. 

<img width="1220" height="895" alt="image" src="https://github.com/user-attachments/assets/52f011b1-dfa8-4e84-9ee9-50450ef635f1" />

**Application Layer** This layer provides entwork services directly to applications. This is like the end uder layer where everything happens that you as a user interact with. Web browsing, file transfers and emails are all handled here in this layer. Protocols that are used in this layer are HTTP which is used for accessing websites and web services, and FTP which is the File Transfer Protocol that is used to transfer files between different servers - SMTP protocl for emails etc. 

<img width="719" height="472" alt="image" src="https://github.com/user-attachments/assets/73e9e556-c19e-4654-a51c-36986213a77f" />

**TCP/IP layers** has four layers and is a more condensed version of the OSI model. 

**Application Layer** this layer is where network applications and their protocols operate such as HTTP, TLS and DNS.

**Transport Layer** this layer is where data transfer between devices happens and the protocols here are TCP and UDP

**Internet Layer** is responsible for logical addressing and routing data across different networks, the primary protocol for this is IP which handles the delivery of your packets from the source to the destination across multiple networks.  

**Network Access Layer** is a condensed version of the Layer 1 and 2 of the OSI model. This layer encompasses things like the physical and data line aspect e.g. Ethernet, Wirless and LAN.

<img width="1444" height="882" alt="image" src="https://github.com/user-attachments/assets/82744956-f331-4767-81cb-56583c9778e6" />


**What the OSI layer looks like for the Sender and Receiver**

Sender
---
<img width="1795" height="913" alt="image" src="https://github.com/user-attachments/assets/a9a4f861-0a76-4e68-9c4d-71f230391b26" />

Application Layer - a POST request is sent with som JSON data included to the HTTPS server 

Presentation Layer - The JSON needs to be serialized meaning you're converting your data which comes in flat byte data string and is then transmitted over the network

Session Layer - Where the establishment, maintenance and termination of connections is done - This case we request to establish TCP connection or TLS for secure comms via HTTPS

Transport Layer - Responsible for delivery the data across the network - The device will send a SYN request (TCP handshake= SYN then SYN-ACK

Receiver
---
<img width="1499" height="878" alt="image" src="https://github.com/user-attachments/assets/8ef6b6e3-6b25-4791-92fe-1bcab1282bff" />

