
- Applies the concept of RPC to distributed objects 
	- invoke methods on an object that exists in another process
- It is generally the same as RPC in terms of options for **interfaces call semantics** and **transparency **
- It also allows object oritent concepts 
- Allows references to objects to be passed over the network

### Distributed Objects 
- Each object encapsulates its own state 
	- different objects in teh same system can be hosted by different processes
- Adopting the clinet server paradigm invoking a method on an object in another process is an **RMI**
- A remote object reference represents a particular object anywhere within a distributed system
- A remote interface specifies which of an object methods can be invoked remotely 

### Implementation 
![[Pasted image 20230217122729.png]]
![[Pasted image 20230217122739.png]]

### Summary 
- **RMI** extends this concept to disributed objects 
- **remote reference** represents a remote object
	- including the server process host and port + object identifier 
- A remote object is represented by a dynamically created proxy object 
	- presents the same 