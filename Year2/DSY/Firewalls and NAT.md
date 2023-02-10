
## Firewalls 
- An organisational fireall is essentially a router 
- it is places between an organization and the internet for protection 
	- packet filter 
- Defines a secure perimeter taht prevents outsiders from interfering with the organisations computers 
- A machine can also have its own firewall 
### Firewall Implementation with a packet filter 
- A manager confgures the packet filter by specifying which packets can pass in each direction
- Based on IP addresses and application port numbers 
- May also examine payload
	- **Deep packet inspection**

## NAT

- **Network Address Locations**
- Devices change the local IP addresses and ports when the yapss on packets 
- usually part of a router - used in most home routers and many corporate networks
- **outside**
	- looks like one IP addresses
- **Inside**
	- Whole private network that uses specfic private IP addresses
- The NAT device swaps between prviate and public IP addresses as packets are forwarded out of and into the private network

- Local addresses can be reused around the world 
- But private IP addresses dont work from other networks 
- THe NAT device can be configured to allow incoming connections to specifci machines / ports 