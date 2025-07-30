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
