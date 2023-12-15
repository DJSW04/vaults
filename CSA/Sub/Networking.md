[[Communication and Networking]]
# Network Topology
---
- [ ] *To understand physical star topology and explain it's operation*
- [ ] *To understand logical bus network topology and explain it's operation*
---
**Topology refers to the structure of a network**
### Star Topology
In a physical star network, each client has a direct connection to the central hub, which receives and delivers packets to the correct recipient. A server can be added to the network in the same way as clients are connected to the hub.
![](https://upload.wikimedia.org/wikipedia/commons/thumb/8/84/Star_Topology.png/220px-Star_Topology.png)
#### Advantages and disadvantages of star topology
[+] Packets are sent directly to their recipient, over a cable that is connected only to the recipient. Other clients on the network cannot see packets that aren’t intended for them.
[+] It is easy to add and remove clients to and from the network.
[+] Each cable has just one device communicating over it, eliminating the possibility of collisions.
[+] The failure of one cable does not affect the performance of the rest of the network.
[-] Should the central hub fail, all communication over the network is stopped.
[-] Expensive to install thanks to the amount of cable required.
[-] Requires specialist staff to maintain

### Logical bus network topology
>A network arrangement where every host computer is connected to a single main data cable

A physical bus connects clients to a single cable, the backbone, with a terminator at each end. Unlike physical star networks, there's no need for a central hub, and a server can be connected to the backbone like a client.
![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/47/BusNetwork.svg/220px-BusNetwork.svg.png)
A logical bus network delivers packets to all clients on the network whereas a logical star network delivers packets only to their recipient.

#### Advantages and disadvantages of a logical bus network topology
[+] There is no central hub, reducing the chances of a network failure and decreasing the cost of installation.
[+] Inexpensive to install as a minimum length of cable is required.
[-] Packets are sent through the shared backbone, allowing every client on the network to see packets that aren’t intended for them.
[-] The backbone is used for communication by multiple clients, introducing the risk of collisions. 
[-] Should the backbone fail, the entire network becomes unusable.

# Types of Networking between Hosts
---
- [ ] *Explain the following and describe situations where they might be used:*
	● peer-to-peer networking 
	● client-server networking
---
### P2P Networking
Peer-to-peer networks eliminate the need for a central server, with each client providing services and holding equal status. For instance, one client could manage print queues, another storage, and a third emails.
![](https://upload.wikimedia.org/wikipedia/commons/thumb/9/9e/P2P_network.svg/200px-P2P_network.svg.png)
#### Advantages and disadvantages of P2P
[-] all clients providing services must be operational for the network to function. If the client managing storage is off or malfunctioning, network users can't access their files.
[+] peer-to-peer networking is more cost-effective than client-server networking as it doesn't require a powerful server. Additionally, peer-to-peer networks are simpler to set up and maintain than their client-server counterparts.

##### Use of P2P
Large file-sharing networks and multimedia providers use peer-to-peer networking to provide high-performance services without the requirement for a server.

### Client-Server Networking 
In a client-server network, central servers provide services to the clients. These servers, often more powerful than the clients, are connected to the network like clients. Clients request services from the servers, which then provide the requested service. These services can include file storage, email management, user account management, and print queue management.
![](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c9/Client-server-model.svg/250px-Client-server-model.svg.png)
##### Use of Client-Server Networking
Most schools, colleges and businesses use client-server networks to allow for central management of clients on the network. This can improve security but requires a fair degree of expertise to set up and manage.
# Wireless Networking
---
- [ ] *Explain the purpose of Wi-Fi* 
- [ ] *Be familiar with the components required for wireless networking* 
- [ ] *Be familiar with how wireless networks are secured* 
- [ ] *Explain the wireless protocol Carrier Sense Multiple Access with Collision Avoidance (CSMA/CA) with and without Request to Send/Clear to Send (RTS/CTS)* 
- [ ] *Be familiar with the purpose of Service Set Identifier (SSID)*
---
Wireless networks enable clients to communicate within a network without physical connection. They require a wireless access point, which connects to a wired network like any other client, and a wireless network adapter in the device connecting to the wireless network.

