
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
	- presents the same interface 
	- converts local invocations in network requests
- A **dispatcher** in the server process passes network requests to the original object 

## Java RMI

### Serializable vs Remote 

- Arguments and return values can be :
	- **primitive** types e.g. int 
		- converted to a stantard external representation and sent to the other processes
	- Instances which implements java.io.**Serializable**
		- converted to standard external representation
		- creates a new object in the remote process with the same class and field values 
	- instances which implement java.rmi.**remote**
		- a new remote reference to be created a sent 
		- tells the receiving process how to create a new proxy for the remote object
			- handles local invocation of its methods and relays them back to the original process and object 

### Summary 

- A remote interface is a java interface that extends **java.rmi.remote**
	- interface types can be primitve serializable or remote
	- remote methods throw java.rmi.remoteExcepton
- The implementation class extends java.rmi.UnicastRemoteObject
- When a reference to a remote object is passed to another process the runtime system creates a proxy object in the new process
- The java **RMI registry** provides a standard **broker** facility to locate remote server object via the **naming** interface 