![image](https://github.com/user-attachments/assets/28218466-6b8b-4cac-baf2-3391dea627b4)


| Proposed Solution       | Pros                                                                 | Cons                                                    | Cost  | Complexity | Potential impact on system performance                                      |
|-------------------------|----------------------------------------------------------------------|---------------------------------------------------------|-------|------------|--------------------------------------------------------------------------------|
| **Adding More Servers** | - Increases system capacity.                                         | - Higher cost due to server purchases                   | High  | Medium     | Reduces individual server load and improves response time.                   |
|                         | - Reduces load on individual servers.                                | - Increased complexity in load balancing.               |       |            |                                                                                |
|                         | - Scalable for future traffic growth.                                | - More servers to monitor and maintain.                 |       |            |                                                                                |
| **Optimization and Caching** | - Reduces system load by storing frequent services and responses in memory. | - Cache monitoring complexity.                           | Medium| High       | Reduces load on servers, improves response times.                            |
|                         | - Improves response times for heavy operations.                      |                                                         |       |            |                                                                                |
| **Security Measures**   | - Protects against malicious attacks like Denial of Service.         | - Potential cost for advanced security services and licenses. | Medium| High       | May add slight latency but helps maintain system integrity and uptime.       |
|                         | - Ensures service availability during traffic spikes.                | - Requires setup and monitoring.                         |       |            |                                                                                |










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




Core Layer:
Includes 2 Multilayer Switches, 2 Perimeter Firewalls, and connections to external ISPs (ISP_1 and ISP_2).
Handles high-speed interconnectivity and external access.

Distribution and Access Layer:
There are 3 Internal Firewalls for securing communication.
6 Switches that is divided to 3 primary and 3 backup switches for redundancy.
Links the core layer with the access layer.
Access Layer:
Features load balancers and multiple servers (Server0 to Server8).

