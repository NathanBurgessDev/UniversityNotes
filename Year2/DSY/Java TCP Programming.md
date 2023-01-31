### Java TCP API
- `ServerSocket` represents a server TCP socket
	- bound to a particular port 
	- waiting to accept connecton requests from client sockets
- `Socket` represents one end of a TCP connection
	- Explicitly created by a client with a specified sever IP address and port number 
	- returned from `accept` in server
	- can be queried for local and reote addresses and port numbers 
	- has na `java.io.InputStream` to receive bytes from and a `java.io.OutputStream` to send bytes to

### TCP Client 

![[Pasted image 20230131112745.png]]

### TCP Considerations 
- **Message Size**  - application reads / writes any number of bytes at a time until the connection is closed 
	- App does not see any message boundaries
	- needs to communicated any message boundaries explicitly in the bytes sent 
- **Message destinations** - a server can accept connection requests from any client 
	- once the connection is esablished then bytes are communicated only between that pair of processes 
- **blocking** - a limited amount of data is buffered at sender and receiver sockets and sends will **block** once the sender buffer is full
	- **flow control** 
	- connecting to a sever
	- acception a connection 
	- and reading from a socket normally block
- **Failure model** - COmmunication is reliable short of complete connection failure
	- lost messages are automatically retransmitted
	- duplicate packets are discarded and out of order packets are re-ordered
	- if a loss is not resolved within a time limit
		- connection fails

### Summary

- **TCP** proved a reliable connection oriented bidirectional byte based stream service
	- 