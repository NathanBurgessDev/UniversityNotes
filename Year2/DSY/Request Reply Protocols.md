
### Overview
- Typical pattern for **Client server interaction**
	- Clinet sends request
	- server recieves
	- server handles
	- server sends responce
	- client recieves responce and continues 
![[Pasted image 20230207143557.png]]


### Request reply API / data requirements 
- Within the client the server needs to be identified by a remote reference
	- IP address
	- Port number
	- Other 
- Server may support several different operations
	- Specificed by operation ID
	- e.g. index of operation, operation name 
- Client and server must agree on how arguemtns are encoded 
- Client normally blocks until the responce is received 
	- Can be **reply-less** (one way) or **asynchronous** 

### Message Structure 

- 

