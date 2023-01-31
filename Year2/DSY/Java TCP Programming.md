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
-**Messa