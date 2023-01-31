
### Message based communication 
- Processes, channels and messages 
![[Pasted image 20230131111409.png]]
- Messages are sent and received via sender and receiver **Queues / buffers**
- The sender performs a send operation
- reciever gets a receive operation
- each endpoint is represented by a socket 


### Sockets
- provides an abstract representation of a communication endpoint within a process
	- TCP, UDP
	- Each protocol has its own specific type of socket
- To send a receive messages a socket must be bound to a specific port
	- a socket may also be bound to a specific internet address 
	- or associated with any internet address
- A single process can have many sockets but only one TCP server or UDP oskcet on a host can be bound to a given port at any time
	- Expect or muticast datagram sockets
	- TCP clients use unused random ports and TCP client / connection sockets must match both the local AND remote ports and addresses
![[Pasted image 20230131111905.png]]


### Message destinations
- for TCP / UDP - sent to the pair
	- Internet address, port number 
		- IP address identifies the host machine
		- port number identifies the process within the host 
		- servers typically use well known ports  i.e. port 8- HTTP
- If a client identifies a sever using a specific IP address then the sever must always have that IP address
- If clients use names then a name server is used to translate this to net work location at run time 
	- DNS - name -> IP address
	- Broker services - service name -> IP address / port number 

### Address resolution 
- In addition to the socket abstraction every OS also provides an API for host name resolution 
- In java
	``` Java
InetAddress aComputer =  
InetAddress.getByName("bruno.dcs.qmul.ac.uk");
```
- Internally the host will use DNS and/ or other name services to look up the corresponding IP address

### Java Socket Programming Summary
- A socket represents a TCP or UDP communication