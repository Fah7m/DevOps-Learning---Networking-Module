# DevOps-Learning---Networking-Module

The networking module is a core module that I enjoyed as I thought it was going to be much harder and complex than I imagined. 

In this readme I will document some key points learnt in this module for quick access or a quick read




🏁Assignment 
---

The assignment for the end of the networking module was to:

-Buy a domain via AWS Route53 or Cloudflare
-Create and EC2 running NGINX on port 80 and add an A record to Route53/Cloudflare.

The objective of this was to be able to access NGINX on the web browser via a domain e.g. (f1him.com).


**Instructions**

1. **Purchase a domain with AWS Route53**

<img width="946" height="580" alt="image" src="https://github.com/user-attachments/assets/1c69af21-7119-48d8-85f8-78ac9098fc51" />


2. **Launch an EC2 Instance with the following specs**
   AMI: Amazon Linux 2023
   Instance Type: t2.micro
   Security Group Inb Rules:

Make sure that you have a **Key Pair** (pem) file downloaded locally so you can ssh safely onto the EC2 instance

<img width="436" height="113" alt="image" src="https://github.com/user-attachments/assets/9fe470ca-d056-43c5-84cf-5fbf1dcf73f6" />

3. **Launching and configuring the EC2**

Give permissions to the key file so you can SSH
```
chmod 400 nginx2.pem
```

SSH with the private key on your terminal
```
ssh -i "nginx.pem" ec2-user@ec2-54-152-214-251.compute-1.amazonaws.com
```

Run the following commands to get NGINX web server running

```
# Update packages
sudo dnf update -y

# Install Nginx
sudo dnf install nginx -y

# Start and enable it
sudo systemctl start nginx
sudo systemctl enable nginx

# Adding text to the webserver to view on browser
echo "Hello from Amazon Linux 2023!" | sudo tee /usr/share/nginx/html/index.html
```

4. **Create records and point them to your Web Server**

First create the records and copy the Public IP of your EC2 Instance 

🔨Troubleshooting
---

***Troubleshooting commands that can be used***

1. dig/nslookup google.com  - to verify any issues with DNS
2. ping IP/google.com - to check if the network is fine
3. traceroute google.com - to check the path the data packet is taking - if I search google.com i want to know the path my network or data packet is taking e.g. going through my computer, to the router to a different network
   until it reaches the final endpoint
