
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
- Every networked machine is a node or host
- Every host has one or more IP addresses
- Any machine can send a packet of data to any other machine
	- aka a **datagram**
		- pakcet size liited to 64kb often less
- Packets may be lost, delayed corrupted or duplicated, although there is some checking for corrupted data
	- **best effort service**

### The internet: layer 3 as seen from layer 4
![[Pasted image 20230203121905.png]]


### TCP and UDP: Streams and messages
- Applications dont use IP directly
	- use one or more transport protocols, TCP or UDP
- **TCP** provides a reliable bidirectional connection oriented service for streams of bytes
	- it uses failure masking techniques covnered in a later lecture
- UDP provides a **best effort connectionless** service for messages = packets of bytes
- Each application within a host is identified by a protocol specific **port** number

## Routing and Configuration 

### Routing and forwarding
- Routers have interfaces on two or more networks and forward packets from one network to the next
- Host and routers have oruting tables
	- identify for each destiniation IP address which interface / host to send it to next
- Hosts and routers work together to deliver each packet to it

