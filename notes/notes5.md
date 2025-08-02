Subnetting
---

Subnetting is the process of dividing a network into much smaller and manageable networks. This improve network management and efficiency

***CIDR Block*** stands for Classless Inter-Domain Routing and this is important because its a method of allocating IP addresses and routing IP packets. 

The format of this is below:

<img width="571" height="287" alt="image" src="https://github.com/user-attachments/assets/20851a39-9e78-4f0a-bf6c-511b951fb848" />

The first part **192.168.1.0/24** is the network address and the **/24** indicates the first 24 bits which is the network apart of the address which leavs the remaining 8 bits for the host addresses.


💡**CIDR is essential for subnetting** 

| IP Range          | 192.168.1.0 – 192.168.1.255 |
| ----------------- | --------------------------- |
| Network address   | 192.168.1.0                 |
| First usable IP   | 192.168.1.1                 |
| Last usable IP    | 192.168.1.254               |
| Broadcast address | 192.168.1.255               |
| Total addresses   | 256                         |
| Usable addresses  | 254                         |



Understanding Binary 
---

Computers and networking devices store and transmit data using binary, because they're built on circuits that are either on (1) or off (0). 

IPv4 addresses are 32 bits long, written as 4 decimal octets:

```
192.168.1.10
```

Each of those numbers (like 192) is an 8-bit number — called an octet.


**Here we have 192 broken down into a binary**

<img width="821" height="415" alt="image" src="https://github.com/user-attachments/assets/a896dd0d-47f8-44f9-8c22-c10518579de4" />

***COMEBACK TO THIS***


Calculating Subnets
---

<img width="1039" height="866" alt="image" src="https://github.com/user-attachments/assets/ca3e7830-a21f-4904-aad5-7803ce47e929" />


In this example we have the IP **192.168.1.0/26** and can see the range of ips that are available. 64 are aviable and 2 will be used for Host and broadcast address.

| Type              | Address      |
| ----------------- | ------------ |
| Network address   | 192.168.1.0  |
| First usable host | 192.168.1.1  |
| Last usable host  | 192.168.1.62 |
| Broadcast address | 192.168.1.63 |


We know in IPv4 addresses that there is 32 bits and we can see that it says /26 in the IP meaning the first 26 bits are reserved for the network and the remaining 6 is for network and broadcast addresses. 

From that we do the below because in each remaning bit there is 2. 
```
2x2x2x2x2x2=64
```

Now we get 64 remaining IP and 2 are always reserved for the Network address and Broadcast gateway.


Network Address Translation
---

NAT basically translates private IP addresses to a public IP address. It essentially groups private IPs into one signle public IP that can be used on the internet. This is important because the without it, each device 
would need its own public IP to access the internet and this is not practical gicen the limited number of public IP addresses. 

The internet doesn't understand private IPs so NAT converts this to a public one that the internet understands in the process below.

<img width="1822" height="806" alt="image" src="https://github.com/user-attachments/assets/7b55a496-5392-4038-8578-7a204e0e6202" />

**Types of NAT**:

***Static NAT*** - This maps a signle private IP to a single public IP addr. This is ideal for servers that need to have public access so the mapping doesn't change which can affect DNS records or Firewall rules.

```
Private IP: 192.168.1.10  →  Public IP: 203.0.113.5
```

****Dynamic NAT*** - This isnt like static mapping where it is one Private IP to one Public IP. In this case we have the Private IP that can map to many Public IP from a pool. It assigna  temporary public IP from a 
pool when needed.

```
Private IP 192.168.1.10 or 192.168.1.11 or 192.168.1.12
```
Can map to IPs from this pool
```
203.0.113.10 > 203.0.113.14 (5 public IPs)
```

***PAT*** - Port Address Translation is known as NAT Overload because it's super efficient. It allows multiple devices on a local network to be mapped to a single Public IP addr but with different port numbers for each
connection.

<img width="974" height="593" alt="image" src="https://github.com/user-attachments/assets/a248690f-f64a-4fe8-be5d-05fd1db33b8c" />

**PAT is useful because:**

  1. You can have hundreds ot Thoursands of devices using a single public IP - good for home networks, offices, cloud VPCs
  2. Scales easily
  3. Priv IPs are hidden from the internet and only allowed connections get replies
  4. Unline Static of Dynamic, PAT doesn't need a pool of public IPS


Benefit of NAT in devops
---

<img width="1760" height="594" alt="image" src="https://github.com/user-attachments/assets/3e75574c-ebee-4e16-961e-84687fe15fa4" />
