DNS - The internet phonebook 
---

In simple terms DNS (Domain Name System) translates domain names like https://wwww.google.com to IP addresses so that you can navigate through the internet.

It simplifies internet navigation for us becuase we don't have to remember every websites IP address when we want to go into but instead we just remember it by it's Domain Name (google.com).


**DNS has many components that help DNS function properly, Two of these are Name Servers and Zone files**

***Name Servers*** serves a crucial role for DNS functionality, they load DNS settings and configurations and respond to queries from clients or other servers about domain names. 

There are two types, **Authoritative and Recursive**

Authoratitative name servers hold the actual DNS records and when queried, they provide definitive answers such as the IP address for a domain name.

Recursive name servers do not hold the final answer and instead, they query other name servers on behalf of the client to find the correct DNS recovers - Recursive servers can also cache information they retrieve to speed up future queries.

The command below can be used to search for a domain to find out more information about it on a UNIX interface

```
dig +short ns google.com
```

<img width="685" height="281" alt="image" src="https://github.com/user-attachments/assets/d854a05b-1b8a-4bbb-9113-49e809b06afb" />


**Zone files are another DNS components that are stored inside your name servers and they contain information about the domain**

They help name servers answer queries about how to get to a domain if the name server doesn't know the answer directly. Zone files organize your DNS information in a readable and manageable way, making it easier to handle DNS records. 

<img width="1210" height="593" alt="image" src="https://github.com/user-attachments/assets/c03b1cfa-69ac-40c4-8a64-f9c187f470b4" />


**DNS Records** - Zone files are comprised of multiple resource records.Each of these records contains information about hosts, nameservers and various other resources. 

Components of resource records are:

Record name - The record name being the domain name being queried 

TTL - Time to live is what indicates how long the record is valid before a refresher is required (new ssl?)

Class - The namespace of the record information

Type - A records, quadruple A records (AAAA), MX records etc. 

Data - The actual information corresponding to a record type - if you have an A record this will be your IP address of IPv4 and if you have a quadruple AAAA this will be IPv6

<img width="1572" height="630" alt="image" src="https://github.com/user-attachments/assets/94d385dd-6253-45f4-a54a-603a9d874732" />


Different records 
---

<img width="1729" height="580" alt="image" src="https://github.com/user-attachments/assets/41adf9ce-0ef3-4fa0-996d-0befe8ab3689" />


A records 
---

A records are known as Address Record and this maps to the domain name to an IPv4 address e.g. 216.58.204.79 - most common type of DNS records and is essential for directing traffic to the correct IP address.

The brother which is the quad A record **(AAAA)** - Simply maps domain to IPv6 such as the below address in the picture

<img width="1487" height="711" alt="image" src="https://github.com/user-attachments/assets/6fd2bc72-77f2-4ca7-ab67-476277133626" />


CNAME records 
---

Canonical name records essentially creates an alias for your domain name e.g. www.google.com is an alias for google.com - This makes DNS management much easier by allowing you to point multiple domain names to the same IP addr.

Think of it by having to type wwww.google.com each time but instead it shortens this for you with an alias.

<img width="1499" height="428" alt="image" src="https://github.com/user-attachments/assets/055335c9-c15e-44ed-9a36-de88f3067e4d" />


MX Records 
---

Mail exchange records specify the mail server responsible for receiving email for a domain e.g. mail-server.google.com would be the MX record for google.com. 

MX records have a priority value which means when you have multiple mail servers that are specified, the priority determintes the order in which servers are tried - low values indicate high priority etc. MX is essential for routing emails to correct mail servers making sure emails email delivery is reliable.

<img width="1444" height="342" alt="image" src="https://github.com/user-attachments/assets/9c0cc61a-f0de-4066-be55-c41a8693d7e8" />


TXT Records 
---

This allows domain admins like Network, Devops engineers to insert any text into DNS. Purpose of this could be verifying that you actually own the domain, or to insert meta data or for email verification (DMARC or DKIM).

<img width="1456" height="353" alt="image" src="https://github.com/user-attachments/assets/8c4f644f-83aa-4c4a-afe2-1b7faaf45712" />



DNS Hierachy 
---

***The DNS root*** doesn't store details about specific domains but rather it keeps high-level information on where to find the top-level domains underneath it.

***The TKD*** include familiar extensions like .com or .org e.g. Verisign manage the .com registry. Each TLD stores information about domains within the scope just like department heads know employees in their department.

***The authoratative name server*** are like manages who oversee specific teams. Each auth nae server hosts zones for domains which means they have detailed DNS records for those domains. E.g. Google.com or X.com have their own DNS records stored there.

***The domain itself*** is where the zone and zone files are located. The zone file will have a list of records for that domain like IP addr, Mail servers etc and the Zone will basically just be the scope that the zone is responsible for - meaning if a sub domain is hosted on another DNS then it will have its own zone and zone file. 

<img width="1830" height="905" alt="image" src="https://github.com/user-attachments/assets/673abb95-2b14-4a35-b5c5-268eb5162814" />


DNS Resolution Process 
---

**Typed google.com into a browseer** 
> A request is sent to the DNS resolver that is local to you 
> DNS resolver does a query and starts looking for the IP addr  
> It checks the local cache first to see if it knows the IP 
> It queries the root server to search for the IP 
> The root server doesn't know the IP yet but knows where to find the .com TLD server 
> TLD server doesn't know the exact IP address of google.com but it knows which Auth name server to ask 
> Resolver queries the auth name server for google.com and the IP address is returned to the DNS resolve which is finally sent back to you

<img width="1813" height="982" alt="image" src="https://github.com/user-attachments/assets/6f320f09-3dfa-46f1-af2c-900bb370f644" />

<img width="1683" height="892" alt="image" src="https://github.com/user-attachments/assets/9b624a37-4e33-42a1-8fb3-d4a9d51a40b2" />


Domain Registrar and DNS hosting provider 
---

DNS registrar - The entity allows you to purchase and register domains - They have a relationship with the TLD registries for various TLD's. It communicates with the TLD registry to manage domain registrations like Go Daddy, Cloudflare and router 53.

DNS hosting prov - This entity operates DNS name servers that host DNS zones - They allow you to manage these DNS records within these zones e.g. Route 53 hosting zone.


**nslookup** is used to query DNS servers - it provides information about DNS records for that certain domain.

```
nslookup google.com
```

<img width="1174" height="579" alt="image" src="https://github.com/user-attachments/assets/189da4c7-f44a-4228-ac6d-af024c046734" />


**dig** stands for Domain Information Grouper and it provides are much more detailed output for querying DNS servers.

```
dig google.com - gives the full output

dig +short google.com - gives just IPs

dig +short ns google.com - gives the name servers
```
<img width="713" height="418" alt="image" src="https://github.com/user-attachments/assets/7acbec8c-4725-43b4-8bc5-7219d73cd921" />


/etc/hosts
---

A local file on your computer that maps omain names to IP addresses. It can also set a rule for domains to use a specific IP address so when doing a search it first looks in the /etc/host file.
