
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
	- Expect or muticas