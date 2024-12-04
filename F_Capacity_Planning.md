First Design
![image](https://github.com/user-attachments/assets/28218466-6b8b-4cac-baf2-3391dea627b4)






Updated Design
![F_Capacity_Planning](https://github.com/user-attachments/assets/7115bb04-d1c3-483e-a254-d82ff3a8a0de)

ISP Redundancy: Two ISPs are included, providing redundant internet access in case one ISP goes down.

Primary and Backup Switches: 
They are connected to both the firewalls and the servers, ensuring failover capability for network traffic.

Critical Servers: 
These servers are now part of a high-availability design, with load balancers managing traffic and the backup switches offering network redundancy.

Load Balancers:
The load balancers are positioned in front of the server clusters, which will distribute the traffic across the servers. This ensures even load distribution and redundancy.

Server Clusters:
Server clusters (e.g., Server0, Server1, Server2) connected to both primary and backup switches, ensuring there is redundancy in the network paths.
These servers are connected to the load balancer, and should one server fail, the load balancer will redirect traffic to the active servers.

Redundancy in Switches:
Both the primary switches and backup switches are connected to the internal firewalls, ensuring that there is no single point of failure in the network.

Redundant Firewalls:
Multiple internal firewalls, which adds an extra layer of security while maintaining redundancy.
