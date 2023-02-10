
## Secuirty Model 

- Security of a dsitributed system can be achieved by **security** the **processes** and the **channels** used for their interacts and by **protecting** the **objects** that they encapsulate against unautherorized access

### Protecting Objects 

- A **server** manages a collection of **objects**
	- on behalf of some users 
- Users run **client** programs which send **invocation** requests to the server to perform operations on the objects 
- **access rights** - specify who is allowed to perform teh operation s of a object 
- Each request is associated with a **principle** - the authority on which it is issued 
![[Pasted image 20230210144626.png]]

- The **server** is responsible for
	- encofrcing access rights of each object
	- verifying the identify of the pronciple behind each request
- The **client** may
	- check the identify of the principle behind the server 
	- to ensure 
- 