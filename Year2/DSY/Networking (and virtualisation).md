
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

### layer 3 as seen from Layer 4
![[Pasted image 20230203122915.png]]

### Internet Model
- Every networked machine is a node or host
- Every host has one or more IP addresses
- Any machine can send a packet of data to any other machine
	- aka a **datagram**
		- pakcet size liited to 64kb often less
- Packets may be lost, delayed corrupted or duplicated, although there is some checking for corrupted data
	- **best effort service**

### Layer 4 as seen from Layer 5
![[Pasted image 20230203123036.png]]

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
- Hosts and routers work together to deliver each packet to its destination hop by hop

### Host Configuration
- Every host on the internet needs to know (for its routing table)
	- ITs own IP
	- IP address range on its local network
	- Ip address of one or more routers (Often gcalled a gateway or default route)
	- (Usually the IP address of a DNS server)
- often discovered when the machine connects to a local network using **DHCP**
- Severs may be statically configured 


## Router Configuration 
- Routers are partly configured statically with
	- IP address for each of its own network interfaces
	- IP address range for each directly connected network
	- other...
- Routers use **Routing Protocols** to exchange information with other routers
	- OSPF within an orginization 
	- BGP between oranisations
	- To determine what routers and links exists, what networks are where and if links are down
	- A routing algorithm can then build a complete routing table 

### Expanded Java TCP example 
![[Pasted image 20230203123101.png]]
![[Pasted image 20230203123114.png]]
## Virtual Machines, Containers, The Cloud and SSH

### Machines, Virtual Machines and Containers 
![[Pasted image 20230203122806.png]]

### VM & Container Networking Components
![[Pasted image 20230203123202.png]]

### Virtual Machine & Container Networking options
![[Pasted image 20230203123235.png]]

### The Cloud 
- Software managed
- On demand
- Pay as you go 

- Many different kinds of services available
	![[Pasted image 20230203123339.png]]

### SSH ( Secure SHell)
- SSH is a network protocol allowing secure remote access hosts over TCP
- An SSH server accepts and authenticates connections (port 22) against local users 
- If successful - creates an **interactive shell** session running as that user 
![[Pasted image 20230203123457.png]]

### Low Level Networking Summary
- Networking relies on **layered** stacks of protocols 
- **Layer 1** deals with signals and direct communication
- **Layer 2** deals with Single hop communciation

### Internet Summary
- Based on TCP IP 
- Every host has at least 1 IP address
- Any host can send a **packet** or **datagram** of data to any other host with **best effort** services
- **Applications** within a signle host are identified by protocol specific port numbers

### Network Configuartion SUmmary
- Each physical has its own rnage of IP addresses
- Each interface on that network has its own IP address
- Routers forward packets between networks 
- Hosts and routers have rotuing tables which determine where to send a packet next 

### VM, Containers and the CLoud Summary
- A **Hypervisor** allows efficent virtualization of a single computer to create multiple isolated **Virtual Machines**
	- Each VM has its own operating System
- A single machine can run multiple **containers** which share the same OS kernel but have a separate runtime and (generally) run one application 
- Each VM or container has it's own **virtual network interface** and IP address
	- These may be visable directly on the physical network
	- or only on a local virtual network with slected ports exposed through **network address translation**
-