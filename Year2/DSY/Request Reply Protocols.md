
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

![[Pasted image 20230207144806.png]]

### Implementation Notes

- Message Identifiers 
	- Each request is given a unique ID 
		- Sender Assigned sequence numbers - *requestid*
		- Sender Identification - IP and Port 
	- Used to
		- Match responces to requests - at client
		- Detect duplicate requests / responces 
- Failure Model
	- can suffer from communication omission faults
		- Lost request or reply
	- process omission faults
		- server or client crash
- Timeouts
	- Client typically uses a timeout to detect a missing reply
		- client retransmits the request
		- but the problem could be a lost request, lost reply or crashed server
- Duplicate request messages 
	- can be detected in the server from the duplicate message identifier
		- if the responce has not been sent yet then no action is needed
		- if the responce has already been sent then the responce will need to be sent again
- History
	- with *indempotent* operations performing the operation twice makes no difference 
		- with other operations the server shoudld not execute a duplicate request twice
		- so the result(s) are held in a history and re-sent back to the client if a duplicate request is received 

### TCP vs UDP

| TCP                         | UD                                                       |
| --------------------------- | -------------------------------------------------------- |
| Establish connection first  | No connection overhead                                   |
| Request = stream of bytes   | Request = 1 message                                      |
| Reply = stream of bytes     | Reply = 1 message                                        |
| No size limit               | limited to a few kB  (fragmentation mangifies loss rate) |
| Reliably delivered in order | May be lost or out of order                              |
| HTTP, SMTP                  | DNS, DHCP                                                |


