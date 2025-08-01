Routing 
---

Routing is the processing of determining the best paths for your data to travel across networks. 

Routing make sure data reaches its destination quickly and efficiently - without routing our data will take forever to get to its destination or lost. 

Routing tables are used to make decisions and Routers determine the best path 

***Importance of Routing in Devops*** 

1. Network performance optimization - If you have a good route and an effective one, this will ensure that your data packets take the most efficient path to reduce latency therefore meaning the overall network performance
   is good and much faster.
   
2. Reliable application delivery - Proper routing is crucial for delivery applications and services especially in complex cloud envrionments.
   
3. Crucial for complex infastructures. Understanding routing and utilizing routing tables efficiently will help you manage these environments more effectively and troubleshoot issues whenever they arise.

<img width="1791" height="660" alt="image" src="https://github.com/user-attachments/assets/25f985b1-c665-4183-88ef-c898f8e3629e" />


Static vs Dynamic Routing 
---

There are two main routing types which are static and dynamic routing.

**Static routing** is essentially a blueprint that is set in place by network admins and is a fixed map for your data to follow. It is reliable but it doesn't adapt well if there are changes or issues on the route. 
If the route changes it will have to be updated manually.

<img width="1790" height="839" alt="image" src="https://github.com/user-attachments/assets/fc745711-8df2-4e9b-b293-55d2aa6f90f0" />

**Dynamic routing** uses algorithms and complex protocols to automatically find the best path for data. It adapts to network changes and if the route is changes, it will automatically recalculate the route if there's a 
roadblock or traffic. It keeps data moving efficiently whatever the circumstance.


<img width="1785" height="836" alt="image" src="https://github.com/user-attachments/assets/dd49d1b0-198f-4b37-9227-63f303aef189" />


***Routing protocols*** automate the process of determining th ebest route for data to travel across a network. Instead of manually setting up routes, these protocols do the heavy lifting. 

The two common routing protocols ares **OSPF and **BGP**

**OSPF** - Open Shortest Path First (OSPF) finds the shortest path for data to travel as the name states. This is used within large orgs and it uses something called a linkstate information which considers the
status of a network, its links, and the cost to use them. OSPF is known for its fast convergency which means it can quickly recalculate routes when there are changes in the network.

**BGP** - Border Gateway Protocol is used to route data between different autonomous systems. It uses something called a path vector mechanism which maintains the path information that gets updated dynamically 
as the network topology changes. BGP allows network admins to define routing policies based on various attributes hence providing the great control over how traffic flows through the network.
