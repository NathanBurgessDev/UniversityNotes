
### Names

- A **name** uniquely distinguishes one thing from another like it
- **Identifiers** are names intended for machine use 
- **Desriptions** are statements about some aspect of a thing 

- A **pure name** is just an array of bits
	- no sturcutre or meaning - just identifies
- An **address** specifically locates a resources
	- good for access
	- bad if the object can move (address not valid)
- Different **services** may use different names 

### URI, URN and URL

- **Uniform Resource Identifiers** - service independent names
	- defined for WWW
- **Uniform Resource Names** - pure names
	- must always be looked up before being used 
- **Uniform Resource Locators** - include information to locate and access a resource 
![[Pasted image 20230224121033.png]]

### Name Services 

- In a **name service** - names are bound to attributes of the resource
	- A name is **resolved** to get these attribute values
- A **name space** is the set of possible names in a name service 
	- name spaces may be flat or hierarchical
	- any given name may be **bound** or **unbound**
	- Name spaces can be subdivided into naming **contexts**
- Name services can be independent of the distributed system
	- may contain names from diff systems (**unification**)
	- may contain names from diff admin domains (**Integration**)
- 