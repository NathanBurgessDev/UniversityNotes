
## Networking 

### Layering

- Lower layers provide services that higher layers build on 

| Layer   | Internet Model |
| --- | ----------- |
| 5   |     Application        |
| 4   |    Transport (TCP,UDP)        |
| 3   |       Internet (IP)      |
| 2   |    Network interface / link         |
| 1   |    Physical         |


| Layer | ISO Model    |
| ----- | ------------ |
| 7     | Application  |
| 6     | Presentation |
| 5     | Session      |
| 4     | Transport    |
| 3     | Network      |
| 2     | Data Link    |
| 1     | Physical             |

### Layer 1 / Layer 2
- Each network can use a diff technology + have different bandwidth latency and reliability 
- Each network interface has its own **Layer 2** Network address **MAC address**
- Some networks allow a signle message to be physically sent to all machines on that network

## The Internet 

- Illusion of a single network provided to users and applications
- Underlying physical structure wth routers interconnecting networks 
- Based on **layer 3** and **layer 4** protocols + supports **layer 5** protocols (DNS, routing)
- Provides a unifying point for almost any network application 
	- doesnt care waht tech / protocol its build on (1 & 2 Layers)
	- Doesnt care what applications it is used for (layer 5)

### Typical Network Protocol Stack
| Layer | Name                     | Common Protocols        | Scope                       |
| ----- | ------------------------ | ----------------------- | --------------------------- |
| 5     | Application              | HTTP,DNS,DHCP,Routing   | Application Specific        |
| 4     | Transport                | TCP, UDP                | Generic Packets and streams |
| 3     | Internet                 | IP (ICMP,ARP)           | Global Communication        |
| 2     | Network Interface (Link) | 802.11 - Ethernet, WiFi | Single hop communication    |
| 1     | Physical                 | Ethernet PHY, ADSL,...  | Signals & Physics                            |

![[Pasted image 20230203121506.png]]

### Internet Model
- Every networked machine is a nod